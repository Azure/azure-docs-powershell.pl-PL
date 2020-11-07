---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerserviceconfig
schema: 2.0.0
ms.openlocfilehash: 4a6f30d1f958094267b4ba8ddf09eb2e342ee889
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899146"
---
# <span data-ttu-id="6ae25-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="6ae25-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="6ae25-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ae25-102">SYNOPSIS</span></span>
<span data-ttu-id="6ae25-103">Tworzy obiekt konfiguracji lokalnej dla usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="6ae25-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ae25-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ae25-104">SYNTAX</span></span>

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

## <span data-ttu-id="6ae25-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ae25-105">DESCRIPTION</span></span>
<span data-ttu-id="6ae25-106">Polecenie cmdlet **New-AzureRmContainerServiceConfig** tworzy obiekt konfiguracji lokalnej dla usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="6ae25-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="6ae25-107">Wprowadź ten obiekt do polecenia cmdlet New-AzureRmContainerService, aby utworzyć usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="6ae25-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="6ae25-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ae25-108">EXAMPLES</span></span>

### <span data-ttu-id="6ae25-109">Przykład 1. Tworzenie konfiguracji usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="6ae25-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="6ae25-110">To polecenie tworzy kontener, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="6ae25-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="6ae25-111">Polecenie określa różne ustawienia konfiguracji usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="6ae25-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="6ae25-112">Polecenie przekazuje obiekt konfiguracji do polecenia cmdlet Add-AzureRmContainerServiceAgentPoolProfile przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="6ae25-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="6ae25-113">Polecenie cmdlet umożliwia dodanie profilu puli agentów.</span><span class="sxs-lookup"><span data-stu-id="6ae25-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="6ae25-114">Określ obiekt w $Container dla parametru *ContainerService* **nowego-AzureRmContainerService**.</span><span class="sxs-lookup"><span data-stu-id="6ae25-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="6ae25-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ae25-115">PARAMETERS</span></span>

### <span data-ttu-id="6ae25-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="6ae25-116">-AdminUsername</span></span>
<span data-ttu-id="6ae25-117">Określa nazwę konta administratora, która ma być używana do obsługi kontenera opartego na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="6ae25-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="6ae25-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="6ae25-118">-AgentPoolProfile</span></span>
<span data-ttu-id="6ae25-119">Określa tablicę obiektów profilu puli agentów dla usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="6ae25-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="6ae25-120">Dodaj profil przy użyciu Add-AzureRmContainerServiceAgentPoolProfile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ae25-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="6ae25-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="6ae25-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="6ae25-122">Określa koordynatora profilów niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="6ae25-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="6ae25-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ae25-123">-DefaultProfile</span></span>
<span data-ttu-id="6ae25-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ae25-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ae25-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6ae25-125">-Location</span></span>
<span data-ttu-id="6ae25-126">Określa lokalizację, w której ma zostać utworzona Usługa kontenera.</span><span class="sxs-lookup"><span data-stu-id="6ae25-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="6ae25-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="6ae25-127">-MasterCount</span></span>
<span data-ttu-id="6ae25-128">Określa liczbę głównych maszyn wirtualnych do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="6ae25-128">Specifies the number of master virtual machines to create.</span></span>

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

### <span data-ttu-id="6ae25-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="6ae25-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="6ae25-130">Określa prefiks DNS dla głównej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6ae25-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="6ae25-131">-Orchestratortype</span><span class="sxs-lookup"><span data-stu-id="6ae25-131">-OrchestratorType</span></span>
<span data-ttu-id="6ae25-132">Określa typ koordynatora usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="6ae25-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="6ae25-133">Dopuszczalne wartości tego parametru to: DCOS oraz Swarm.</span><span class="sxs-lookup"><span data-stu-id="6ae25-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="6ae25-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="6ae25-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="6ae25-135">Określa identyfikator klienta profilu głównego.</span><span class="sxs-lookup"><span data-stu-id="6ae25-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="6ae25-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="6ae25-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="6ae25-137">Określa klucz tajny profilu głównego.</span><span class="sxs-lookup"><span data-stu-id="6ae25-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="6ae25-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="6ae25-138">-SshPublicKey</span></span>
<span data-ttu-id="6ae25-139">Określa klucz publiczny SSH dla usługi kontenera opartej na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="6ae25-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="6ae25-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ae25-140">-Tag</span></span>
<span data-ttu-id="6ae25-141">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="6ae25-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6ae25-142">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="6ae25-142">For example:</span></span>

<span data-ttu-id="6ae25-143">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="6ae25-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6ae25-144">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="6ae25-144">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="6ae25-145">Wskazuje, czy ta konfiguracja włącza diagnostykę maszyny wirtualnej usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="6ae25-145">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="6ae25-146">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="6ae25-146">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="6ae25-147">Określa hasło administratora usługi kontenera korzystającej z systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="6ae25-147">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="6ae25-148">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="6ae25-148">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="6ae25-149">Określa nazwę użytkownika administratora usługi kontenera korzystającej z systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="6ae25-149">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="6ae25-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ae25-150">-Confirm</span></span>
<span data-ttu-id="6ae25-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ae25-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ae25-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ae25-152">-WhatIf</span></span>
<span data-ttu-id="6ae25-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ae25-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ae25-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ae25-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ae25-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ae25-155">CommonParameters</span></span>
<span data-ttu-id="6ae25-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ae25-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ae25-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ae25-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ae25-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ae25-158">INPUTS</span></span>

### <span data-ttu-id="6ae25-159">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6ae25-159">None</span></span>
<span data-ttu-id="6ae25-160">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6ae25-160">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ae25-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ae25-161">OUTPUTS</span></span>

### <span data-ttu-id="6ae25-162">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="6ae25-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="6ae25-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ae25-163">NOTES</span></span>

## <span data-ttu-id="6ae25-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ae25-164">RELATED LINKS</span></span>

[<span data-ttu-id="6ae25-165">Dodaj-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="6ae25-165">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="6ae25-166">Nowe — AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6ae25-166">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)
