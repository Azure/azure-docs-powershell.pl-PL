---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 76719250ca7909d86d288b987b9598a58ab5fb88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706105"
---
# <span data-ttu-id="c2daa-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="c2daa-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="c2daa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2daa-102">SYNOPSIS</span></span>
<span data-ttu-id="c2daa-103">Umożliwia utworzenie grupy kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="c2daa-103">Creates a container group.</span></span>

## <span data-ttu-id="c2daa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2daa-104">SYNTAX</span></span>

### <span data-ttu-id="c2daa-105">CreateContainerGroupBaseParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c2daa-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2daa-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="c2daa-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2daa-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="c2daa-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2daa-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2daa-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2daa-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c2daa-109">DESCRIPTION</span></span>
<span data-ttu-id="c2daa-110">Polecenia cmdlet **New-AzContainerGroup** tworzą grupę kontenerów.</span><span class="sxs-lookup"><span data-stu-id="c2daa-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="c2daa-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2daa-111">EXAMPLES</span></span>

### <span data-ttu-id="c2daa-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2daa-112">Example 1</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="c2daa-113">To polecenie tworzy grupę kontenerów przy użyciu najnowszego obrazu Nginx i żąda publicznego adresu IP z otwartym portem 8000.</span><span class="sxs-lookup"><span data-stu-id="c2daa-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="c2daa-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c2daa-114">Example 2</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="c2daa-115">To polecenie powoduje utworzenie grupy kontenerów i uruchomienie niestandardowego skryptu w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="c2daa-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="c2daa-116">Przykład 3: Tworzenie grupy kontenerów uruchamianie-ukończenie.</span><span class="sxs-lookup"><span data-stu-id="c2daa-116">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="c2daa-117">To polecenie tworzy grupę kontenerów, w której zostanie wydrukowany "cześć" i zatrzymana.</span><span class="sxs-lookup"><span data-stu-id="c2daa-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="c2daa-118">Przykład 4: Tworzenie grupy kontenerów przy użyciu obrazu w rejestrze kontenera platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c2daa-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myacr}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="c2daa-119">To polecenie tworzy grupę kontenerów przy użyciu obrazu Nginx w rejestrze kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2daa-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="c2daa-120">Przykład 5: Tworzenie grupy kontenerów przy użyciu obrazu w rejestrze niestandardowego obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="c2daa-120">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="c2daa-121">To polecenie tworzy grupę kontenerów przy użyciu obrazu niestandardowego z rejestru niestandardowego obrazu kontenera.</span><span class="sxs-lookup"><span data-stu-id="c2daa-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="c2daa-122">Przykład 6: Tworzenie grupy kontenerów instalujących wolumin plików platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c2daa-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image alpine -AzFileVolumeShareName myshare -AzFileVolumeAccountKey $mycred -AzFileVolumeMountPath /mnt/azfile

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  : {AzureFile}
State                    : Running
Events                   : {}
```

<span data-ttu-id="c2daa-123">To polecenie tworzy grupę kontenerów, która instaluje udostępniony udział plików w usłudze Azure `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="c2daa-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="c2daa-124">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="c2daa-124">Example 7</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -AssignIdentity

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="c2daa-125">To polecenie tworzy grupę kontenerów z zapisaną tożsamością system za pomocą najnowszego obrazu Nginx i żąda publicznego adresu IP z otwartym portem 8000.</span><span class="sxs-lookup"><span data-stu-id="c2daa-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="c2daa-126">Przykład 8</span><span class="sxs-lookup"><span data-stu-id="c2daa-126">Example 8</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -IdentityType SystemAssignedUserAssigned -IdentityId /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<UserIdentityName>

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="c2daa-127">To polecenie tworzy grupę kontenerów z przypisanym systemem i tożsamością przypisaną przez użytkownika przy użyciu najnowszego obrazu Nginx i żąda publicznego adresu IP z otwartym portem 8000.</span><span class="sxs-lookup"><span data-stu-id="c2daa-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="c2daa-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2daa-128">PARAMETERS</span></span>

### <span data-ttu-id="c2daa-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c2daa-129">-AssignIdentity</span></span>
<span data-ttu-id="c2daa-130">Włączanie tożsamości przypisanej do systemu</span><span class="sxs-lookup"><span data-stu-id="c2daa-130">Enable system assigned identity</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateContainerGroupBaseParamSet, CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="c2daa-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="c2daa-132">Poświadczenie konta magazynu w udziale plików platformy Azure do zainstalowania, gdzie nazwa użytkownika jest nazwą konta magazynu, a kluczem jest klucz konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c2daa-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="c2daa-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="c2daa-134">Ścieżka instalacji dla woluminu plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2daa-134">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="c2daa-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="c2daa-136">Nazwa udziału plików platformy Azure do zainstalowania.</span><span class="sxs-lookup"><span data-stu-id="c2daa-136">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-137">-Command</span><span class="sxs-lookup"><span data-stu-id="c2daa-137">-Command</span></span>
<span data-ttu-id="c2daa-138">Polecenie, które ma zostać uruchomione w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="c2daa-138">The command to run in the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-139">-Procesor</span><span class="sxs-lookup"><span data-stu-id="c2daa-139">-Cpu</span></span>
<span data-ttu-id="c2daa-140">Wymagane rdzenie procesora.</span><span class="sxs-lookup"><span data-stu-id="c2daa-140">The required CPU cores.</span></span>
<span data-ttu-id="c2daa-141">Wartość domyślna: 1</span><span class="sxs-lookup"><span data-stu-id="c2daa-141">Default: 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2daa-142">-DefaultProfile</span></span>
<span data-ttu-id="c2daa-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2daa-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="c2daa-144">-DnsNameLabel</span></span>
<span data-ttu-id="c2daa-145">Etykieta nazwy DNS dla adresu IP.</span><span class="sxs-lookup"><span data-stu-id="c2daa-145">The DNS name label for the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-146">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="c2daa-146">-EnvironmentVariable</span></span>
<span data-ttu-id="c2daa-147">Zmienne środowiskowe kontenera.</span><span class="sxs-lookup"><span data-stu-id="c2daa-147">The container environment variables.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-148">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="c2daa-148">-IdentityId</span></span>
<span data-ttu-id="c2daa-149">Identyfikator tożsamości przypisany użytkownikowi</span><span class="sxs-lookup"><span data-stu-id="c2daa-149">The user assigned identity IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c2daa-150">-IdentityType</span></span>
<span data-ttu-id="c2daa-151">Zarządzany typ tożsamości</span><span class="sxs-lookup"><span data-stu-id="c2daa-151">The managed identity type</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerInstance.Models.ResourceIdentityType
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet, ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-152">-Image</span><span class="sxs-lookup"><span data-stu-id="c2daa-152">-Image</span></span>
<span data-ttu-id="c2daa-153">Obraz kontenera.</span><span class="sxs-lookup"><span data-stu-id="c2daa-153">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-154">-Adres_iptype</span><span class="sxs-lookup"><span data-stu-id="c2daa-154">-IpAddressType</span></span>
<span data-ttu-id="c2daa-155">Typ adresu IP.</span><span class="sxs-lookup"><span data-stu-id="c2daa-155">The IP address type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-156">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c2daa-156">-Location</span></span>
<span data-ttu-id="c2daa-157">Lokalizacja grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="c2daa-157">The container group Location.</span></span>
<span data-ttu-id="c2daa-158">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2daa-158">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-159">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="c2daa-159">-MemoryInGB</span></span>
<span data-ttu-id="c2daa-160">Wymagana pamięć w GB.</span><span class="sxs-lookup"><span data-stu-id="c2daa-160">The required memory in GB.</span></span>
<span data-ttu-id="c2daa-161">Wartość domyślna: 1,5</span><span class="sxs-lookup"><span data-stu-id="c2daa-161">Default: 1.5</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: Memory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-162">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2daa-162">-Name</span></span>
<span data-ttu-id="c2daa-163">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="c2daa-163">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-164">-OsType</span><span class="sxs-lookup"><span data-stu-id="c2daa-164">-OsType</span></span>
<span data-ttu-id="c2daa-165">Typ systemu operacyjnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="c2daa-165">The container OS type.</span></span>
<span data-ttu-id="c2daa-166">Wartość domyślna: Linux</span><span class="sxs-lookup"><span data-stu-id="c2daa-166">Default: Linux</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Linux, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-167">-Port</span><span class="sxs-lookup"><span data-stu-id="c2daa-167">-Port</span></span>
<span data-ttu-id="c2daa-168">Liczba portów do otwarcia.</span><span class="sxs-lookup"><span data-stu-id="c2daa-168">The port(s) to open.</span></span> <span data-ttu-id="c2daa-169">Wartość domyślna: [80]</span><span class="sxs-lookup"><span data-stu-id="c2daa-169">Default: [80]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c2daa-170">-RegistryCredential</span></span>
<span data-ttu-id="c2daa-171">Poświadczenia rejestru niestandardowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="c2daa-171">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="c2daa-172">-RegistryServerDomain</span></span>
<span data-ttu-id="c2daa-173">Serwer logowania rejestru niestandardowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="c2daa-173">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2daa-174">-ResourceGroupName</span></span>
<span data-ttu-id="c2daa-175">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2daa-175">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="c2daa-176">-RestartPolicy</span></span>
<span data-ttu-id="c2daa-177">Zasady ponownego uruchamiania kontenera.</span><span class="sxs-lookup"><span data-stu-id="c2daa-177">The container restart policy.</span></span> <span data-ttu-id="c2daa-178">Domyślne: zawsze</span><span class="sxs-lookup"><span data-stu-id="c2daa-178">Default: Always</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Always, Never, OnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2daa-179">-Tag</span></span>
<span data-ttu-id="c2daa-180">{{Opis znacznika Fill}}</span><span class="sxs-lookup"><span data-stu-id="c2daa-180">{{Fill Tag Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-181">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2daa-181">-Confirm</span></span>
<span data-ttu-id="c2daa-182">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2daa-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2daa-183">-WhatIf</span></span>
<span data-ttu-id="c2daa-184">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2daa-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2daa-185">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c2daa-185">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2daa-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2daa-186">CommonParameters</span></span>
<span data-ttu-id="c2daa-187">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2daa-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2daa-188">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2daa-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2daa-189">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2daa-189">INPUTS</span></span>

### <span data-ttu-id="c2daa-190">System. String</span><span class="sxs-lookup"><span data-stu-id="c2daa-190">System.String</span></span>

### <span data-ttu-id="c2daa-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="c2daa-191">System.String[]</span></span>

### <span data-ttu-id="c2daa-192">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c2daa-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c2daa-193">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2daa-193">OUTPUTS</span></span>

### <span data-ttu-id="c2daa-194">Microsoft. Azure. Commands. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="c2daa-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="c2daa-195">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2daa-195">NOTES</span></span>

## <span data-ttu-id="c2daa-196">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2daa-196">RELATED LINKS</span></span>