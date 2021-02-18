---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 20daa8d14f77ca4563c072d58d1c2269235cb164
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181506"
---
# <span data-ttu-id="094ab-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="094ab-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="094ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="094ab-102">SYNOPSIS</span></span>
<span data-ttu-id="094ab-103">Tworzy grupę kontenera.</span><span class="sxs-lookup"><span data-stu-id="094ab-103">Creates a container group.</span></span>

## <span data-ttu-id="094ab-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="094ab-104">SYNTAX</span></span>

### <span data-ttu-id="094ab-105">CreateContainerGroupBaseParamSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="094ab-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="094ab-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="094ab-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="094ab-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="094ab-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="094ab-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="094ab-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="094ab-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="094ab-109">DESCRIPTION</span></span>
<span data-ttu-id="094ab-110">Polecenia **cmdlet New-AzContainerGroup** tworzą grupę kontenera.</span><span class="sxs-lookup"><span data-stu-id="094ab-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="094ab-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="094ab-111">EXAMPLES</span></span>

### <span data-ttu-id="094ab-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="094ab-112">Example 1</span></span>
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

<span data-ttu-id="094ab-113">Te polecenia tworzą grupę kontenerów przy użyciu najnowszego obrazu nginx i żąda publicznego adresu IP z otwarciem portu 8000.</span><span class="sxs-lookup"><span data-stu-id="094ab-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="094ab-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="094ab-114">Example 2</span></span>
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

<span data-ttu-id="094ab-115">Te polecenia tworzą grupę kontenerów i uruchamiają skrypt niestandardowy wewnątrz kontenera.</span><span class="sxs-lookup"><span data-stu-id="094ab-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="094ab-116">Przykład 3. Tworzy grupę kontenera uruchamianą do ukończenia.</span><span class="sxs-lookup"><span data-stu-id="094ab-116">Example 3: Creates a run-to-completion container group.</span></span>
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

<span data-ttu-id="094ab-117">Te polecenia tworzą grupę kontenerów, która drukuje słowo "witaj" i zatrzymuje się.</span><span class="sxs-lookup"><span data-stu-id="094ab-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="094ab-118">Przykład 4. Tworzenie grupy kontenera przy użyciu obrazu w rejestrze kontenerów platformy Azure</span><span class="sxs-lookup"><span data-stu-id="094ab-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
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

<span data-ttu-id="094ab-119">Te polecenia tworzą grupę kontenerów przy użyciu obrazu nginx w rejestrze kontenerów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="094ab-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="094ab-120">Przykład 5. Tworzenie grupy kontenerów przy użyciu obrazu w niestandardowym rejestrze obrazów kontenera</span><span class="sxs-lookup"><span data-stu-id="094ab-120">Example 5: Creates a container group using image in custom container image registry</span></span>
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

<span data-ttu-id="094ab-121">Te polecenia tworzą grupę kontenerów przy użyciu obrazu niestandardowego z rejestru obrazów kontenera niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="094ab-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="094ab-122">Przykład 6. Tworzy grupę kontenerów, która umożliwia uchwytowanie woluminu plików platformy Azure</span><span class="sxs-lookup"><span data-stu-id="094ab-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name mycontainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountCredential $mycred -AzureFileVolumeMountPath /mnt/azfile

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

<span data-ttu-id="094ab-123">Te polecenia tworzą grupę kontenerów, w ramach których jest chowywny podany udział plików platformy `/mnt/azfile` Azure.</span><span class="sxs-lookup"><span data-stu-id="094ab-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="094ab-124">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="094ab-124">Example 7</span></span>
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

<span data-ttu-id="094ab-125">Te polecenia tworzą grupę kontenerów z przypisaną tożsamością systemu przy użyciu najnowszego obrazu nginx i żąda publicznego adresu IP z otwarciem portu 8000.</span><span class="sxs-lookup"><span data-stu-id="094ab-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="094ab-126">Przykład 8</span><span class="sxs-lookup"><span data-stu-id="094ab-126">Example 8</span></span>
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

<span data-ttu-id="094ab-127">To polecenie tworzy grupę kontenerów z przypisaną tożsamością systemu i przypisaną przez użytkownika przy użyciu najnowszego obrazu nginx i żąda publicznego adresu IP z otwarciem portu 8000.</span><span class="sxs-lookup"><span data-stu-id="094ab-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="094ab-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="094ab-128">PARAMETERS</span></span>

### <span data-ttu-id="094ab-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="094ab-129">-AssignIdentity</span></span>
<span data-ttu-id="094ab-130">Włącz tożsamość przypisaną przez system</span><span class="sxs-lookup"><span data-stu-id="094ab-130">Enable system assigned identity</span></span>

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

### <span data-ttu-id="094ab-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="094ab-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="094ab-132">Poświadczenia konta magazynu udziału plików platformy Azure do instalacji, gdzie nazwa użytkownika jest nazwą konta magazynu, a kluczem jest klucz konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="094ab-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

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

### <span data-ttu-id="094ab-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="094ab-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="094ab-134">Ścieżka instalacji dla woluminu plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="094ab-134">The mount path for the Azure File volume.</span></span>

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

### <span data-ttu-id="094ab-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="094ab-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="094ab-136">Nazwa udziału plików platformy Azure do instalacji.</span><span class="sxs-lookup"><span data-stu-id="094ab-136">The name of the Azure File share to mount.</span></span>

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

### <span data-ttu-id="094ab-137">- Command</span><span class="sxs-lookup"><span data-stu-id="094ab-137">-Command</span></span>
<span data-ttu-id="094ab-138">Polecenie uruchamiane w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="094ab-138">The command to run in the container.</span></span>

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

### <span data-ttu-id="094ab-139">— Procesor</span><span class="sxs-lookup"><span data-stu-id="094ab-139">-Cpu</span></span>
<span data-ttu-id="094ab-140">Wymagane rdzenie procesora.</span><span class="sxs-lookup"><span data-stu-id="094ab-140">The required CPU cores.</span></span>
<span data-ttu-id="094ab-141">Domyślne: 1</span><span class="sxs-lookup"><span data-stu-id="094ab-141">Default: 1</span></span>

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

### <span data-ttu-id="094ab-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="094ab-142">-DefaultProfile</span></span>
<span data-ttu-id="094ab-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="094ab-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="094ab-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="094ab-144">-DnsNameLabel</span></span>
<span data-ttu-id="094ab-145">Etykieta nazwy DNS dla adresu IP.</span><span class="sxs-lookup"><span data-stu-id="094ab-145">The DNS name label for the IP address.</span></span>

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

### <span data-ttu-id="094ab-146">—EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="094ab-146">-EnvironmentVariable</span></span>
<span data-ttu-id="094ab-147">Zmienne środowiskowe kontenera.</span><span class="sxs-lookup"><span data-stu-id="094ab-147">The container environment variables.</span></span>

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

### <span data-ttu-id="094ab-148">- IdentityId</span><span class="sxs-lookup"><span data-stu-id="094ab-148">-IdentityId</span></span>
<span data-ttu-id="094ab-149">Identyfikatory tożsamości przypisane przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="094ab-149">The user assigned identity IDs</span></span>

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

### <span data-ttu-id="094ab-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="094ab-150">-IdentityType</span></span>
<span data-ttu-id="094ab-151">Typ tożsamości zarządzanej</span><span class="sxs-lookup"><span data-stu-id="094ab-151">The managed identity type</span></span>

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

### <span data-ttu-id="094ab-152">— Obraz</span><span class="sxs-lookup"><span data-stu-id="094ab-152">-Image</span></span>
<span data-ttu-id="094ab-153">Obraz kontenera.</span><span class="sxs-lookup"><span data-stu-id="094ab-153">The container image.</span></span>

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

### <span data-ttu-id="094ab-154">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="094ab-154">-IpAddressType</span></span>
<span data-ttu-id="094ab-155">Typ adresu IP.</span><span class="sxs-lookup"><span data-stu-id="094ab-155">The IP address type.</span></span>

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

### <span data-ttu-id="094ab-156">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="094ab-156">-Location</span></span>
<span data-ttu-id="094ab-157">Lokalizacja grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="094ab-157">The container group Location.</span></span>
<span data-ttu-id="094ab-158">Domyślna lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="094ab-158">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="094ab-159">— MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="094ab-159">-MemoryInGB</span></span>
<span data-ttu-id="094ab-160">Wymagana pamięć w GB.</span><span class="sxs-lookup"><span data-stu-id="094ab-160">The required memory in GB.</span></span>
<span data-ttu-id="094ab-161">Domyślne: 1,5</span><span class="sxs-lookup"><span data-stu-id="094ab-161">Default: 1.5</span></span>

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

### <span data-ttu-id="094ab-162">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="094ab-162">-Name</span></span>
<span data-ttu-id="094ab-163">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="094ab-163">The container group name.</span></span>

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

### <span data-ttu-id="094ab-164">- OsType</span><span class="sxs-lookup"><span data-stu-id="094ab-164">-OsType</span></span>
<span data-ttu-id="094ab-165">Typ systemu operacyjnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="094ab-165">The container OS type.</span></span>
<span data-ttu-id="094ab-166">Domyślne: Linux</span><span class="sxs-lookup"><span data-stu-id="094ab-166">Default: Linux</span></span>

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

### <span data-ttu-id="094ab-167">— Port</span><span class="sxs-lookup"><span data-stu-id="094ab-167">-Port</span></span>
<span data-ttu-id="094ab-168">Port(y) do otwarcia.</span><span class="sxs-lookup"><span data-stu-id="094ab-168">The port(s) to open.</span></span> <span data-ttu-id="094ab-169">Domyślne: [80]</span><span class="sxs-lookup"><span data-stu-id="094ab-169">Default: [80]</span></span>

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

### <span data-ttu-id="094ab-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="094ab-170">-RegistryCredential</span></span>
<span data-ttu-id="094ab-171">Poświadczenia rejestru kontenera niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="094ab-171">The custom container registry credential.</span></span>

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

### <span data-ttu-id="094ab-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="094ab-172">-RegistryServerDomain</span></span>
<span data-ttu-id="094ab-173">Niestandardowy serwer logowania kontenera.</span><span class="sxs-lookup"><span data-stu-id="094ab-173">The custom container registry login server.</span></span>

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

### <span data-ttu-id="094ab-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="094ab-174">-ResourceGroupName</span></span>
<span data-ttu-id="094ab-175">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="094ab-175">The resource group name.</span></span>

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

### <span data-ttu-id="094ab-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="094ab-176">-RestartPolicy</span></span>
<span data-ttu-id="094ab-177">Zasady ponownego uruchamiania kontenera.</span><span class="sxs-lookup"><span data-stu-id="094ab-177">The container restart policy.</span></span> <span data-ttu-id="094ab-178">Domyślne: Zawsze</span><span class="sxs-lookup"><span data-stu-id="094ab-178">Default: Always</span></span>

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

### <span data-ttu-id="094ab-179">— Tag</span><span class="sxs-lookup"><span data-stu-id="094ab-179">-Tag</span></span>
<span data-ttu-id="094ab-180">{{Fill Tag Description}}</span><span class="sxs-lookup"><span data-stu-id="094ab-180">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="094ab-181">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="094ab-181">-Confirm</span></span>
<span data-ttu-id="094ab-182">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="094ab-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="094ab-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="094ab-183">-WhatIf</span></span>
<span data-ttu-id="094ab-184">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="094ab-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="094ab-185">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="094ab-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="094ab-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="094ab-186">CommonParameters</span></span>
<span data-ttu-id="094ab-187">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="094ab-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="094ab-188">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="094ab-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="094ab-189">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="094ab-189">INPUTS</span></span>

### <span data-ttu-id="094ab-190">System.String</span><span class="sxs-lookup"><span data-stu-id="094ab-190">System.String</span></span>

### <span data-ttu-id="094ab-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="094ab-191">System.String[]</span></span>

### <span data-ttu-id="094ab-192">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="094ab-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="094ab-193">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="094ab-193">OUTPUTS</span></span>

### <span data-ttu-id="094ab-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="094ab-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="094ab-195">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="094ab-195">NOTES</span></span>

## <span data-ttu-id="094ab-196">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="094ab-196">RELATED LINKS</span></span>
