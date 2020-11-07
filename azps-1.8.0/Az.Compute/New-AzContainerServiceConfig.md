---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: cf335717fbe1507d84ec9ada80efb9f06332c004
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710286"
---
# <span data-ttu-id="1ee9e-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="1ee9e-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="1ee9e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ee9e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee9e-103">Tworzy obiekt konfiguracji lokalnej dla usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="1ee9e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ee9e-104">SYNTAX</span></span>

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

## <span data-ttu-id="1ee9e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ee9e-105">DESCRIPTION</span></span>
<span data-ttu-id="1ee9e-106">Polecenie cmdlet **New-AzContainerServiceConfig** tworzy obiekt konfiguracji lokalnej dla usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="1ee9e-107">Wprowadź ten obiekt do polecenia cmdlet New-AzContainerService, aby utworzyć usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="1ee9e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ee9e-108">EXAMPLES</span></span>

### <span data-ttu-id="1ee9e-109">Przykład 1. Tworzenie konfiguracji usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="1ee9e-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="1ee9e-110">To polecenie tworzy kontener, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="1ee9e-111">Polecenie określa różne ustawienia konfiguracji usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="1ee9e-112">Polecenie przekazuje obiekt konfiguracji do polecenia cmdlet Add-AzContainerServiceAgentPoolProfile przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="1ee9e-113">Polecenie cmdlet umożliwia dodanie profilu puli agentów.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="1ee9e-114">Określ obiekt w $Container dla parametru *ContainerService* **nowego-AzContainerService**.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="1ee9e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ee9e-115">PARAMETERS</span></span>

### <span data-ttu-id="1ee9e-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="1ee9e-116">-AdminUsername</span></span>
<span data-ttu-id="1ee9e-117">Określa nazwę konta administratora, która ma być używana do obsługi kontenera opartego na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="1ee9e-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="1ee9e-118">-AgentPoolProfile</span></span>
<span data-ttu-id="1ee9e-119">Określa tablicę obiektów profilu puli agentów dla usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="1ee9e-120">Dodaj profil przy użyciu Add-AzContainerServiceAgentPoolProfile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="1ee9e-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="1ee9e-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="1ee9e-122">Określa koordynatora profilów niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="1ee9e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ee9e-123">-DefaultProfile</span></span>
<span data-ttu-id="1ee9e-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ee9e-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1ee9e-125">-Location</span></span>
<span data-ttu-id="1ee9e-126">Określa lokalizację, w której ma zostać utworzona Usługa kontenera.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="1ee9e-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="1ee9e-127">-MasterCount</span></span>
<span data-ttu-id="1ee9e-128">Określa liczbę głównych maszyn wirtualnych do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-128">Specifies the number of master virtual machines to create.</span></span>

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

### <span data-ttu-id="1ee9e-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="1ee9e-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="1ee9e-130">Określa prefiks DNS dla głównej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="1ee9e-131">-Orchestratortype</span><span class="sxs-lookup"><span data-stu-id="1ee9e-131">-OrchestratorType</span></span>
<span data-ttu-id="1ee9e-132">Określa typ koordynatora usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="1ee9e-133">Dopuszczalne wartości tego parametru to: DCOS oraz Swarm.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="1ee9e-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="1ee9e-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="1ee9e-135">Określa identyfikator klienta profilu głównego.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="1ee9e-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="1ee9e-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="1ee9e-137">Określa klucz tajny profilu głównego.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="1ee9e-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="1ee9e-138">-SshPublicKey</span></span>
<span data-ttu-id="1ee9e-139">Określa klucz publiczny SSH dla usługi kontenera opartej na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="1ee9e-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="1ee9e-140">-Tag</span></span>
<span data-ttu-id="1ee9e-141">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1ee9e-142">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="1ee9e-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1ee9e-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="1ee9e-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="1ee9e-144">Wskazuje, czy ta konfiguracja włącza diagnostykę maszyny wirtualnej usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="1ee9e-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="1ee9e-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="1ee9e-146">Określa hasło administratora usługi kontenera korzystającej z systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="1ee9e-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="1ee9e-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="1ee9e-148">Określa nazwę użytkownika administratora usługi kontenera korzystającej z systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="1ee9e-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ee9e-149">-Confirm</span></span>
<span data-ttu-id="1ee9e-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ee9e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ee9e-151">-WhatIf</span></span>
<span data-ttu-id="1ee9e-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ee9e-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ee9e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee9e-154">CommonParameters</span></span>
<span data-ttu-id="1ee9e-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ee9e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee9e-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ee9e-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee9e-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ee9e-157">INPUTS</span></span>

### <span data-ttu-id="1ee9e-158">System. String</span><span class="sxs-lookup"><span data-stu-id="1ee9e-158">System.String</span></span>

### <span data-ttu-id="1ee9e-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1ee9e-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1ee9e-160">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. ContainerServiceOrchestratorTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="1ee9e-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1ee9e-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1ee9e-161">System.Int32</span></span>

### <span data-ttu-id="1ee9e-162">Microsoft. Azure. Management. COMPUTE. MODELES. ContainerServiceAgentPoolProfile []</span><span class="sxs-lookup"><span data-stu-id="1ee9e-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="1ee9e-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="1ee9e-163">System.String[]</span></span>

### <span data-ttu-id="1ee9e-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ee9e-164">System.Boolean</span></span>

## <span data-ttu-id="1ee9e-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ee9e-165">OUTPUTS</span></span>

### <span data-ttu-id="1ee9e-166">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="1ee9e-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="1ee9e-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ee9e-167">NOTES</span></span>

## <span data-ttu-id="1ee9e-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ee9e-168">RELATED LINKS</span></span>

[<span data-ttu-id="1ee9e-169">Dodaj-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="1ee9e-169">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="1ee9e-170">Nowe — AzContainerService</span><span class="sxs-lookup"><span data-stu-id="1ee9e-170">New-AzContainerService</span></span>](./New-AzContainerService.md)