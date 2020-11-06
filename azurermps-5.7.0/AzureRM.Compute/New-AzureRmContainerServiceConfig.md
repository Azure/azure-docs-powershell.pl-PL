---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: 0568359131a91beeb175d69da51d1646bd28f88e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525318"
---
# <span data-ttu-id="d7ab3-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="d7ab3-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="d7ab3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ab3-103">Tworzy obiekt konfiguracji lokalnej dla usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7ab3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7ab3-104">SYNTAX</span></span>

```
New-AzureRmContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7ab3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7ab3-105">DESCRIPTION</span></span>
<span data-ttu-id="d7ab3-106">Polecenie cmdlet **New-AzureRmContainerServiceConfig** tworzy obiekt konfiguracji lokalnej dla usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="d7ab3-107">Wprowadź ten obiekt do polecenia cmdlet New-AzureRmContainerService, aby utworzyć usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="d7ab3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7ab3-108">EXAMPLES</span></span>

### <span data-ttu-id="d7ab3-109">Przykład 1. Tworzenie konfiguracji usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="d7ab3-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="d7ab3-110">To polecenie tworzy kontener, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="d7ab3-111">Polecenie określa różne ustawienia konfiguracji usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-111">The command specifies various settings for the container service configuration.</span></span>
<span data-ttu-id="d7ab3-112">Polecenie przekazuje obiekt konfiguracji do polecenia cmdlet Add-AzureRmContainerServiceAgentPoolProfile przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d7ab3-113">Polecenie cmdlet umożliwia dodanie profilu puli agentów.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="d7ab3-114">Określ obiekt w $Container dla parametru *ContainerService* **nowego-AzureRmContainerService**.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="d7ab3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7ab3-115">PARAMETERS</span></span>

### <span data-ttu-id="d7ab3-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="d7ab3-116">-AdminUsername</span></span>
<span data-ttu-id="d7ab3-117">Określa nazwę konta administratora, która ma być używana do obsługi kontenera opartego na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d7ab3-118">-AgentPoolProfile</span></span>
<span data-ttu-id="d7ab3-119">Określa tablicę obiektów profilu puli agentów dla usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="d7ab3-120">Dodaj profil przy użyciu Add-AzureRmContainerServiceAgentPoolProfile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="d7ab3-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="d7ab3-122">Określa koordynatora profilów niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-122">Specifies the custom profile orchestrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d7ab3-123">-Location</span></span>
<span data-ttu-id="d7ab3-124">Określa lokalizację, w której ma zostać utworzona Usługa kontenera.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-124">Specifies the location in which to create the container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-125">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="d7ab3-125">-MasterCount</span></span>
<span data-ttu-id="d7ab3-126">Określa liczbę głównych maszyn wirtualnych do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-126">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-127">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="d7ab3-127">-MasterDnsPrefix</span></span>
<span data-ttu-id="d7ab3-128">Określa prefiks DNS dla głównej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-128">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-129">-Orchestratortype</span><span class="sxs-lookup"><span data-stu-id="d7ab3-129">-OrchestratorType</span></span>
<span data-ttu-id="d7ab3-130">Określa typ koordynatora usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-130">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="d7ab3-131">Dopuszczalne wartości tego parametru to: DCOS oraz Swarm.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-131">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: ContainerServiceOrchestratorTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-132">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="d7ab3-132">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="d7ab3-133">Określa identyfikator klienta profilu głównego.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-133">Specifies the principal profile client ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-134">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="d7ab3-134">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="d7ab3-135">Określa klucz tajny profilu głównego.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-135">Specifies the principal profile secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-136">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="d7ab3-136">-SshPublicKey</span></span>
<span data-ttu-id="d7ab3-137">Określa klucz publiczny SSH dla usługi kontenera opartej na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-137">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="d7ab3-138">-Tag</span></span>
<span data-ttu-id="d7ab3-139">Określa Tagi usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-139">Specifies tags for the container service.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-140">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="d7ab3-140">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="d7ab3-141">Wskazuje, czy ta konfiguracja włącza diagnostykę maszyny wirtualnej usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-141">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-142">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="d7ab3-142">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="d7ab3-143">Określa hasło administratora usługi kontenera korzystającej z systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-143">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-144">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="d7ab3-144">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="d7ab3-145">Określa nazwę użytkownika administratora usługi kontenera korzystającej z systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-145">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7ab3-146">-Confirm</span></span>
<span data-ttu-id="d7ab3-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7ab3-148">-WhatIf</span></span>
<span data-ttu-id="d7ab3-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7ab3-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ab3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ab3-151">CommonParameters</span></span>
<span data-ttu-id="d7ab3-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ab3-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7ab3-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ab3-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7ab3-154">INPUTS</span></span>

### <span data-ttu-id="d7ab3-155">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d7ab3-155">None</span></span>
<span data-ttu-id="d7ab3-156">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d7ab3-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7ab3-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7ab3-157">OUTPUTS</span></span>

## <span data-ttu-id="d7ab3-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7ab3-158">NOTES</span></span>

## <span data-ttu-id="d7ab3-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7ab3-159">RELATED LINKS</span></span>

[<span data-ttu-id="d7ab3-160">Dodaj-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d7ab3-160">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="d7ab3-161">Nowe — AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="d7ab3-161">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)


