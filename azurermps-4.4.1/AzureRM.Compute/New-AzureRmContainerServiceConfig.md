---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: e88f1d3ce684881d839574fe0b73f36b83e275f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719532"
---
# <span data-ttu-id="e8739-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="e8739-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="e8739-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8739-102">SYNOPSIS</span></span>
<span data-ttu-id="e8739-103">Tworzy obiekt konfiguracji lokalnej dla usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="e8739-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8739-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8739-104">SYNTAX</span></span>

```
New-AzureRmContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8739-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8739-105">DESCRIPTION</span></span>
<span data-ttu-id="e8739-106">Polecenie cmdlet **New-AzureRmContainerServiceConfig** tworzy obiekt konfiguracji lokalnej dla usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="e8739-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="e8739-107">Wprowadź ten obiekt do polecenia cmdlet New-AzureRmContainerService, aby utworzyć usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="e8739-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="e8739-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8739-108">EXAMPLES</span></span>

### <span data-ttu-id="e8739-109">Przykład 1. Tworzenie konfiguracji usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="e8739-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="e8739-110">To polecenie tworzy kontener, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="e8739-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="e8739-111">Polecenie określa różne ustawienia konfiguracji usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="e8739-111">The command specifies various settings for the container service configuration.</span></span>
<span data-ttu-id="e8739-112">Polecenie przekazuje obiekt konfiguracji do polecenia cmdlet Add-AzureRmContainerServiceAgentPoolProfile przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="e8739-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e8739-113">Polecenie cmdlet umożliwia dodanie profilu puli agentów.</span><span class="sxs-lookup"><span data-stu-id="e8739-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="e8739-114">Określ obiekt w $Container dla parametru *ContainerService* **nowego-AzureRmContainerService**.</span><span class="sxs-lookup"><span data-stu-id="e8739-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="e8739-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8739-115">PARAMETERS</span></span>

### <span data-ttu-id="e8739-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="e8739-116">-AdminUsername</span></span>
<span data-ttu-id="e8739-117">Określa nazwę konta administratora, która ma być używana do obsługi kontenera opartego na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="e8739-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="e8739-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e8739-118">-AgentPoolProfile</span></span>
<span data-ttu-id="e8739-119">Określa tablicę obiektów profilu puli agentów dla usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="e8739-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="e8739-120">Dodaj profil przy użyciu Add-AzureRmContainerServiceAgentPoolProfile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8739-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="e8739-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="e8739-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="e8739-122">Określa koordynatora profilów niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="e8739-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="e8739-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8739-123">-DefaultProfile</span></span>
<span data-ttu-id="e8739-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8739-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8739-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e8739-125">-Location</span></span>
<span data-ttu-id="e8739-126">Określa lokalizację, w której ma zostać utworzona Usługa kontenera.</span><span class="sxs-lookup"><span data-stu-id="e8739-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="e8739-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="e8739-127">-MasterCount</span></span>
<span data-ttu-id="e8739-128">Określa liczbę głównych maszyn wirtualnych do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="e8739-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8739-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="e8739-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="e8739-130">Określa prefiks DNS dla głównej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8739-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="e8739-131">-Orchestratortype</span><span class="sxs-lookup"><span data-stu-id="e8739-131">-OrchestratorType</span></span>
<span data-ttu-id="e8739-132">Określa typ koordynatora usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="e8739-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="e8739-133">Dopuszczalne wartości tego parametru to: DCOS oraz Swarm.</span><span class="sxs-lookup"><span data-stu-id="e8739-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="e8739-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="e8739-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="e8739-135">Określa identyfikator klienta profilu głównego.</span><span class="sxs-lookup"><span data-stu-id="e8739-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="e8739-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="e8739-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="e8739-137">Określa klucz tajny profilu głównego.</span><span class="sxs-lookup"><span data-stu-id="e8739-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="e8739-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e8739-138">-SshPublicKey</span></span>
<span data-ttu-id="e8739-139">Określa klucz publiczny SSH dla usługi kontenera opartej na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="e8739-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="e8739-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8739-140">-Tag</span></span>
<span data-ttu-id="e8739-141">Określa Tagi usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="e8739-141">Specifies tags for the container service.</span></span>

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

### <span data-ttu-id="e8739-142">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="e8739-142">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="e8739-143">Wskazuje, czy ta konfiguracja włącza diagnostykę maszyny wirtualnej usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="e8739-143">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="e8739-144">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="e8739-144">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="e8739-145">Określa hasło administratora usługi kontenera korzystającej z systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="e8739-145">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="e8739-146">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="e8739-146">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="e8739-147">Określa nazwę użytkownika administratora usługi kontenera korzystającej z systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="e8739-147">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="e8739-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8739-148">-Confirm</span></span>
<span data-ttu-id="e8739-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8739-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8739-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8739-150">-WhatIf</span></span>
<span data-ttu-id="e8739-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8739-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8739-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8739-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8739-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8739-153">CommonParameters</span></span>
<span data-ttu-id="e8739-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8739-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8739-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8739-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8739-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8739-156">INPUTS</span></span>

## <span data-ttu-id="e8739-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8739-157">OUTPUTS</span></span>

## <span data-ttu-id="e8739-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8739-158">NOTES</span></span>

## <span data-ttu-id="e8739-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8739-159">RELATED LINKS</span></span>

[<span data-ttu-id="e8739-160">Dodaj-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e8739-160">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="e8739-161">Nowe — AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e8739-161">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)


