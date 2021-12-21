<script setup>
import { Menu, MenuButton, MenuItems, MenuItem } from "@headlessui/vue";
import {
  HomeIcon,
  CogIcon,
  UsersIcon,
  PhoneIcon,
} from "@heroicons/vue/outline";
</script>
<template>
  <nav>
    <div class="m-8">
      <h1 class="text-xl font-bold">ドロップダウンメニュー</h1>
      <Menu>
        <MenuButton
          class="
            px-4
            py-2
            border
            rounded-lg
            bg-blue-600
            hover:bg-blue-400
            text-white
            font-bold
          "
          >Menu</MenuButton
        >
        <transition
          enter-active-class="transition duration-300 ease-out"
          enter-from-class="transform scale-95 opacity-0"
          enter-to-class="transform scale-100 opacity-100"
          leave-active-class="transition duration-300 ease-out"
          leave-from-class="transform scale-100 opacity-100"
          leave-to-class="transform scale-95 opacity-0"
        >
          <MenuItems as="ul" class="w-[200px] divide-y border rounded-lg mt-2">
            <MenuItem as="li" v-slot="{ active }">
              <a
                href="/"
                :class="
                  active
                    ? 'bg-violet-500 text-white rounded-t-lg'
                    : 'text-gray-900'
                "
                class="p-2 inline-block flex items-center"
              >
                <HomeIcon class="w-5 y-5 mr-2" />
                Home
              </a>
            </MenuItem>
            <MenuItem as="li" v-slot="{ active }">
              <a
                href="/"
                :class="active ? 'bg-violet-500 text-white' : 'text-gray-900'"
                class="p-2 inline-block flex items-center"
              >
                <CogIcon class="w-5 y-5 mr-2" />
                Service
              </a>
            </MenuItem>
            <MenuItem as="li" v-slot="{ active }">
              <a
                href="/"
                :class="active ? 'bg-violet-500 text-white' : 'text-gray-900'"
                class="p-2 inline-block flex items-center"
              >
                <UsersIcon class="w-5 y-5 mr-2" />
                About Us
              </a>
            </MenuItem>
            <MenuItem as="li" v-slot="{ active }">
              <a
                href="/"
                :class="
                  active
                    ? 'bg-violet-500 rounded-b-lg text-white'
                    : 'text-gray-900'
                "
                class="p-2 inline-block flex items-center"
              >
                <PhoneIcon class="w-5 y-5 mr-2" />
                Contact
              </a>
            </MenuItem>
          </MenuItems>
        </transition>
      </Menu>
    </div>
  </nav>
</template>