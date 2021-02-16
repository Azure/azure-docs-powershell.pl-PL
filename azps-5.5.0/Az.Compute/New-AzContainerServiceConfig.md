---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: a2d55c831860f5664f0f8f3dd5312368a9e5da4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199259"
---
# <span data-ttu-id="fd448-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="fd448-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="fd448-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd448-102">SYNOPSIS</span></span>
<span data-ttu-id="fd448-103">Tworzy obiekt konfiguracji lokalnej dla usługi kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="fd448-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="fd448-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fd448-104">SYNTAX</span></span>

```
New-AzContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd448-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fd448-105">DESCRIPTION</span></span>
<span data-ttu-id="fd448-106">Polecenie **cmdlet New-AzContainerServiceConfig** tworzy obiekt konfiguracji lokalnej dla usługi kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="fd448-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="fd448-107">Udostępnij ten obiekt New-AzContainerService cmdlet, aby utworzyć usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="fd448-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="fd448-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fd448-108">EXAMPLES</span></span>

### <span data-ttu-id="fd448-109">Przykład 1. Tworzenie konfiguracji usługi kontenerowej</span><span class="sxs-lookup"><span data-stu-id="fd448-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="fd448-110">To polecenie tworzy kontener, a następnie przechowuje go w $Container zmienną.</span><span class="sxs-lookup"><span data-stu-id="fd448-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="fd448-111">To polecenie określa różne ustawienia dla konfiguracji usługi kontenerów.</span><span class="sxs-lookup"><span data-stu-id="fd448-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="fd448-112">Polecenie przekazuje obiekt konfiguracji do Add-AzContainerServiceAgentPoolProfile cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="fd448-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="fd448-113">To polecenie cmdlet dodaje profil puli agenta.</span><span class="sxs-lookup"><span data-stu-id="fd448-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="fd448-114">Określ obiekt w $Container *parametru ContainerService* usługi **New-AzContainerService.**</span><span class="sxs-lookup"><span data-stu-id="fd448-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="fd448-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd448-115">PARAMETERS</span></span>

### <span data-ttu-id="fd448-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="fd448-116">-AdminUsername</span></span>
<span data-ttu-id="fd448-117">Określa nazwę konta administratora, która ma być używania dla usługi kontenerowej opartej na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="fd448-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd448-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="fd448-118">-AgentPoolProfile</span></span>
<span data-ttu-id="fd448-119">Określa tablicę obiektów profilu puli agenta dla usługi kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="fd448-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="fd448-120">Dodaj profil za pomocą polecenia cmdlet Add-AzContainerServiceAgentPoolProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd448-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd448-121">-CustomProfileO nietrwale</span><span class="sxs-lookup"><span data-stu-id="fd448-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="fd448-122">Określa niestandardowy program do oznaczania profilów.</span><span class="sxs-lookup"><span data-stu-id="fd448-122">Specifies the custom profile orchestrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd448-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd448-123">-DefaultProfile</span></span>
<span data-ttu-id="fd448-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd448-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd448-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fd448-125">-Location</span></span>
<span data-ttu-id="fd448-126">Określa lokalizację, w której ma być tworzyć usługę kontenerową.</span><span class="sxs-lookup"><span data-stu-id="fd448-126">Specifies the location in which to create the container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd448-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="fd448-127">-MasterCount</span></span>
<span data-ttu-id="fd448-128">Określa liczbę maszyn wirtualnych do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="fd448-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd448-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="fd448-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="fd448-130">Określa prefiks DNS dla głównej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fd448-130">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd448-131">-WertorType</span><span class="sxs-lookup"><span data-stu-id="fd448-131">-OrchestratorType</span></span>
<span data-ttu-id="fd448-132">Określa typatora dla usługi kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="fd448-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="fd448-133">Dopuszczalne wartości dla tego parametru to: DCOS i Swarm.</span><span class="sxs-lookup"><span data-stu-id="fd448-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd448-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="fd448-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="fd448-135">Określa główny identyfikator klienta profilu.</span><span class="sxs-lookup"><span data-stu-id="fd448-135">Specifies the principal profile client ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd448-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="fd448-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="fd448-137">Określa klucz tajny profilu głównego.</span><span class="sxs-lookup"><span data-stu-id="fd448-137">Specifies the principal profile secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd448-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="fd448-138">-SshPublicKey</span></span>
<span data-ttu-id="fd448-139">Określa klucz publiczny SSH dla usługi kontenerowej opartej na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="fd448-139">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd448-140">— Tag</span><span class="sxs-lookup"><span data-stu-id="fd448-140">-Tag</span></span>
<span data-ttu-id="fd448-141">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="fd448-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fd448-142">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="fd448-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd448-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="fd448-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="fd448-144">Wskazuje, czy ta konfiguracja umożliwia korzystanie z diagnostyki dla maszyny wirtualnej usługi kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="fd448-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd448-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="fd448-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="fd448-146">Określa hasło administratora usługi kontenerowej, która korzysta z systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="fd448-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd448-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="fd448-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="fd448-148">Określa nazwę użytkownika administratora usługi kontenerów, która korzysta z systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="fd448-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd448-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd448-149">-Confirm</span></span>
<span data-ttu-id="fd448-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fd448-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd448-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd448-151">-WhatIf</span></span>
<span data-ttu-id="fd448-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd448-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd448-153">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fd448-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd448-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd448-154">CommonParameters</span></span>
<span data-ttu-id="fd448-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd448-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd448-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd448-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd448-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd448-157">INPUTS</span></span>

### <span data-ttu-id="fd448-158">System.String</span><span class="sxs-lookup"><span data-stu-id="fd448-158">System.String</span></span>

### <span data-ttu-id="fd448-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fd448-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fd448-160">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceO przeszł. Typy, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="fd448-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="fd448-161">System.Int32</span><span class="sxs-lookup"><span data-stu-id="fd448-161">System.Int32</span></span>

### <span data-ttu-id="fd448-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceagentPoolProfile[]</span><span class="sxs-lookup"><span data-stu-id="fd448-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="fd448-163">System.String[]</span><span class="sxs-lookup"><span data-stu-id="fd448-163">System.String[]</span></span>

### <span data-ttu-id="fd448-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd448-164">System.Boolean</span></span>

## <span data-ttu-id="fd448-165">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd448-165">OUTPUTS</span></span>

### <span data-ttu-id="fd448-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="fd448-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="fd448-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fd448-167">NOTES</span></span>

## <span data-ttu-id="fd448-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd448-168">RELATED LINKS</span></span>

[<span data-ttu-id="fd448-169">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="fd448-169">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="fd448-170">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="fd448-170">New-AzContainerService</span></span>](./New-AzContainerService.md)
