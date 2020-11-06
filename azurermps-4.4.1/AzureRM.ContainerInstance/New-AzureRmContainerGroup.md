---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 63c54c5f1bb17af82e353b70e757bf91b1208958
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551075"
---
# <span data-ttu-id="a476f-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a476f-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="a476f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a476f-102">SYNOPSIS</span></span>
<span data-ttu-id="a476f-103">Umożliwia utworzenie grupy kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="a476f-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a476f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a476f-104">SYNTAX</span></span>

### <span data-ttu-id="a476f-105">CreateContainerGroupBaseParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a476f-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a476f-106">CreateContainerGroupWithRegistryParamSet</span><span class="sxs-lookup"><span data-stu-id="a476f-106">CreateContainerGroupWithRegistryParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>]
 -RegistryCredential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a476f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a476f-107">DESCRIPTION</span></span>
<span data-ttu-id="a476f-108">Polecenia cmdlet **New-AzureRmContainerGroup** tworzą grupę kontenerów.</span><span class="sxs-lookup"><span data-stu-id="a476f-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="a476f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a476f-109">EXAMPLES</span></span>

### <span data-ttu-id="a476f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a476f-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port 8000

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
```

<span data-ttu-id="a476f-111">To polecenie tworzy grupę kontenerów przy użyciu najnowszego obrazu Nginx i żąda publicznego adresu IP z otwartym portem 8000.</span><span class="sxs-lookup"><span data-stu-id="a476f-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="a476f-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a476f-112">Example 2</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

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
```

<span data-ttu-id="a476f-113">To polecenie powoduje utworzenie grupy kontenerów i uruchomienie niestandardowego skryptu w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="a476f-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="a476f-114">Przykład 3: Tworzenie grupy kontenerów przy użyciu obrazu w rejestrze kontenera platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a476f-114">Example 3: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

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
```

<span data-ttu-id="a476f-115">To polecenie tworzy grupę kontenerów przy użyciu obrazu Nginx w rejestrze kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a476f-115">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="a476f-116">Przykład 4: Tworzenie grupy kontenerów przy użyciu obrazu w rejestrze niestandardowego obrazu kontenera</span><span class="sxs-lookup"><span data-stu-id="a476f-116">Example 4: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

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
```

<span data-ttu-id="a476f-117">To polecenie tworzy grupę kontenerów przy użyciu obrazu niestandardowego z rejestru niestandardowego obrazu kontenera.</span><span class="sxs-lookup"><span data-stu-id="a476f-117">This commands creates a container group using a custom image from a custom container image registry.</span></span>

## <span data-ttu-id="a476f-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a476f-118">PARAMETERS</span></span>

### <span data-ttu-id="a476f-119">-Command</span><span class="sxs-lookup"><span data-stu-id="a476f-119">-Command</span></span>
<span data-ttu-id="a476f-120">Polecenie, które ma zostać uruchomione w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="a476f-120">The command to run in the container.</span></span>

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

### <span data-ttu-id="a476f-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a476f-121">-Confirm</span></span>
<span data-ttu-id="a476f-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a476f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a476f-123">-Procesor</span><span class="sxs-lookup"><span data-stu-id="a476f-123">-Cpu</span></span>
<span data-ttu-id="a476f-124">Wymagane rdzenie procesora.</span><span class="sxs-lookup"><span data-stu-id="a476f-124">The required CPU cores.</span></span>
<span data-ttu-id="a476f-125">Wartość domyślna: 1</span><span class="sxs-lookup"><span data-stu-id="a476f-125">Default: 1</span></span>

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

### <span data-ttu-id="a476f-126">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="a476f-126">-EnvironmentVariable</span></span>
<span data-ttu-id="a476f-127">Zmienne środowiskowe kontenera.</span><span class="sxs-lookup"><span data-stu-id="a476f-127">The container environment variables.</span></span>

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

### <span data-ttu-id="a476f-128">-Image</span><span class="sxs-lookup"><span data-stu-id="a476f-128">-Image</span></span>
<span data-ttu-id="a476f-129">Obraz kontenera.</span><span class="sxs-lookup"><span data-stu-id="a476f-129">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a476f-130">-Adres_iptype</span><span class="sxs-lookup"><span data-stu-id="a476f-130">-IpAddressType</span></span>
<span data-ttu-id="a476f-131">Typ adresu IP.</span><span class="sxs-lookup"><span data-stu-id="a476f-131">The IP address type.</span></span>

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

### <span data-ttu-id="a476f-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a476f-132">-Location</span></span>
<span data-ttu-id="a476f-133">Lokalizacja grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="a476f-133">The container group Location.</span></span>
<span data-ttu-id="a476f-134">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a476f-134">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="a476f-135">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="a476f-135">-MemoryInGB</span></span>
<span data-ttu-id="a476f-136">Wymagana pamięć w GB.</span><span class="sxs-lookup"><span data-stu-id="a476f-136">The required memory in GB.</span></span>
<span data-ttu-id="a476f-137">Wartość domyślna: 1,5</span><span class="sxs-lookup"><span data-stu-id="a476f-137">Default: 1.5</span></span>

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

### <span data-ttu-id="a476f-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a476f-138">-Name</span></span>
<span data-ttu-id="a476f-139">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="a476f-139">The container group name.</span></span>

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

### <span data-ttu-id="a476f-140">-OsType</span><span class="sxs-lookup"><span data-stu-id="a476f-140">-OsType</span></span>
<span data-ttu-id="a476f-141">Typ systemu operacyjnego kontenera.</span><span class="sxs-lookup"><span data-stu-id="a476f-141">The container OS type.</span></span>
<span data-ttu-id="a476f-142">Wartość domyślna: Linux</span><span class="sxs-lookup"><span data-stu-id="a476f-142">Default: Linux</span></span>

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

### <span data-ttu-id="a476f-143">-Port</span><span class="sxs-lookup"><span data-stu-id="a476f-143">-Port</span></span>
<span data-ttu-id="a476f-144">Port do otwarcia.</span><span class="sxs-lookup"><span data-stu-id="a476f-144">The port to open.</span></span>
<span data-ttu-id="a476f-145">Wartość domyślna: 80</span><span class="sxs-lookup"><span data-stu-id="a476f-145">Default: 80</span></span>

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

### <span data-ttu-id="a476f-146">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a476f-146">-RegistryCredential</span></span>
<span data-ttu-id="a476f-147">Poświadczenia rejestru niestandardowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="a476f-147">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a476f-148">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="a476f-148">-RegistryServerDomain</span></span>
<span data-ttu-id="a476f-149">Serwer logowania rejestru niestandardowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="a476f-149">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a476f-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a476f-150">-ResourceGroupName</span></span>
<span data-ttu-id="a476f-151">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a476f-151">The resource group name.</span></span>

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

### <span data-ttu-id="a476f-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="a476f-152">-Tag</span></span>
<span data-ttu-id="a476f-153">{{Opis znacznika Fill}}</span><span class="sxs-lookup"><span data-stu-id="a476f-153">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="a476f-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a476f-154">-WhatIf</span></span>
<span data-ttu-id="a476f-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a476f-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a476f-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a476f-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a476f-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a476f-157">-DefaultProfile</span></span>
<span data-ttu-id="a476f-158">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a476f-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a476f-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a476f-159">CommonParameters</span></span>
<span data-ttu-id="a476f-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a476f-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a476f-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a476f-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a476f-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a476f-162">INPUTS</span></span>

### <span data-ttu-id="a476f-163">System. String</span><span class="sxs-lookup"><span data-stu-id="a476f-163">System.String</span></span>
<span data-ttu-id="a476f-164">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a476f-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a476f-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a476f-165">OUTPUTS</span></span>

### <span data-ttu-id="a476f-166">Microsoft. Azure. Commands. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a476f-166">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="a476f-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a476f-167">NOTES</span></span>

## <span data-ttu-id="a476f-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a476f-168">RELATED LINKS</span></span>

