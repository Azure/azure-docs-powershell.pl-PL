---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8418A93-8E6B-4A1C-B319-7CACE95AB600
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1daf0cb8881beeb71f0b3fe68732d596c56ce12
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055206"
---
# <span data-ttu-id="e9aab-101">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="e9aab-101">Move-AzureService</span></span>

## <span data-ttu-id="e9aab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9aab-102">SYNOPSIS</span></span>
<span data-ttu-id="e9aab-103">Migruje usługę w chmurze do stosu Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e9aab-103">Migrates a cloud service to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="e9aab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9aab-104">SYNTAX</span></span>

### <span data-ttu-id="e9aab-105">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9aab-105">AbortMigrationParameterSet</span></span>
```
Move-AzureService [-Abort] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e9aab-106">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9aab-106">CommitMigrationParameterSet</span></span>
```
Move-AzureService [-Commit] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e9aab-107">PrepareNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9aab-107">PrepareNewMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9aab-108">PrepareExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9aab-108">PrepareExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9aab-109">ValidateNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9aab-109">ValidateNewMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9aab-110">ValidateExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9aab-110">ValidateExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9aab-111">Opis</span><span class="sxs-lookup"><span data-stu-id="e9aab-111">DESCRIPTION</span></span>
<span data-ttu-id="e9aab-112">Polecenie cmdlet **Move-AzureService** migruje usługę w chmurze i wdrożenie w tej usłudze do grupy zasobów na stosie usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="e9aab-112">The **Move-AzureService** cmdlet migrates a cloud service and a deployment inside that service to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="e9aab-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9aab-113">EXAMPLES</span></span>

### <span data-ttu-id="e9aab-114">Przykład 1: przygotowywanie migracji usług</span><span class="sxs-lookup"><span data-stu-id="e9aab-114">Example 1: Prepare service migration</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="e9aab-115">To polecenie przygotowuje usługę o nazwie ContosoService do migracji na stos Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e9aab-115">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="e9aab-116">Migracja obejmuje wdrożenie o nazwie ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="e9aab-116">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="e9aab-117">Przykład 2: uruchamianie migracji usług</span><span class="sxs-lookup"><span data-stu-id="e9aab-117">Example 2: Start service migration</span></span>
```
PS C:\> Move-AzureService -Commit -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="e9aab-118">To polecenie rozpoczyna migrację usługi o nazwie ContosoService na stosie Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e9aab-118">This command starts migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="e9aab-119">Migracja obejmuje wdrożenie o nazwie ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="e9aab-119">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="e9aab-120">Przykład 3: anulowanie migracji usług</span><span class="sxs-lookup"><span data-stu-id="e9aab-120">Example 3: Cancel service migration</span></span>
```
PS C:\> Move-AzureService -Abort -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="e9aab-121">To polecenie anuluje migrację usługi o nazwie ContosoService na stosie Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e9aab-121">This command cancels migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="e9aab-122">Przykład 4: przygotowywanie migracji usług do istniejącej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e9aab-122">Example 4: Prepare service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "VnetRG" -VirtualNetworkName "ContosoVNET" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="e9aab-123">To polecenie przygotowuje usługę o nazwie ContosoService do migracji na stos Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e9aab-123">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="e9aab-124">Migracja obejmuje wdrożenie o nazwie ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="e9aab-124">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="e9aab-125">W ramach migracji jest używana uprzednio utworzona sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="e9aab-125">The migration uses a virtual network that was previously created.</span></span>

### <span data-ttu-id="e9aab-126">Przykład 5: sprawdzanie poprawności migracji usługi</span><span class="sxs-lookup"><span data-stu-id="e9aab-126">Example 5: Validate service migration</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="e9aab-127">To polecenie sprawdza poprawność migracji usługi o nazwie ContosoService na stosie Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e9aab-127">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="e9aab-128">Migracja obejmuje wdrożenie o nazwie ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="e9aab-128">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="e9aab-129">Przykład 6: weryfikowanie migracji usługi do istniejącej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e9aab-129">Example 6: Validate service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "contosoService" -DeploymentName "contosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "vnetRG" -VirtualNetworkName "contosoVNET" -SubnetName "contosoSubnet"
```

<span data-ttu-id="e9aab-130">To polecenie sprawdza poprawność migracji usługi o nazwie ContosoService na stosie Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e9aab-130">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="e9aab-131">Migracja obejmuje wdrożenie o nazwie ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="e9aab-131">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="e9aab-132">W ramach migracji jest używana uprzednio utworzona sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="e9aab-132">The migration uses a virtual network that was previously created.</span></span>

## <span data-ttu-id="e9aab-133">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9aab-133">PARAMETERS</span></span>

### <span data-ttu-id="e9aab-134">-Przerwij</span><span class="sxs-lookup"><span data-stu-id="e9aab-134">-Abort</span></span>
<span data-ttu-id="e9aab-135">Wskazuje, że to polecenie cmdlet anuluje migrację usług.</span><span class="sxs-lookup"><span data-stu-id="e9aab-135">Indicates that this cmdlet cancels the service migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aab-136">-Commit</span><span class="sxs-lookup"><span data-stu-id="e9aab-136">-Commit</span></span>
<span data-ttu-id="e9aab-137">Wskazuje, że to polecenie cmdlet rozpoczyna migrację usługi.</span><span class="sxs-lookup"><span data-stu-id="e9aab-137">Indicates that this cmdlet starts the service migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aab-138">-CreateNewVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e9aab-138">-CreateNewVirtualNetwork</span></span>
<span data-ttu-id="e9aab-139">Wskazuje, że to polecenie cmdlet tworzy sieć wirtualną na stosie usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="e9aab-139">Indicates that this cmdlet creates a virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, ValidateNewMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aab-140">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="e9aab-140">-DeploymentName</span></span>
<span data-ttu-id="e9aab-141">Określa nazwę wdrożenia usługi w chmurze, które to polecenie cmdlet migruje.</span><span class="sxs-lookup"><span data-stu-id="e9aab-141">Specifies the name of the cloud service deployment that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aab-142">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e9aab-142">-InformationAction</span></span>
<span data-ttu-id="e9aab-143">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="e9aab-143">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e9aab-144">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e9aab-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e9aab-145">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="e9aab-145">Continue</span></span>
- <span data-ttu-id="e9aab-146">Ignorować</span><span class="sxs-lookup"><span data-stu-id="e9aab-146">Ignore</span></span>
- <span data-ttu-id="e9aab-147">Inquire</span><span class="sxs-lookup"><span data-stu-id="e9aab-147">Inquire</span></span>
- <span data-ttu-id="e9aab-148">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e9aab-148">SilentlyContinue</span></span>
- <span data-ttu-id="e9aab-149">Przestaw</span><span class="sxs-lookup"><span data-stu-id="e9aab-149">Stop</span></span>
- <span data-ttu-id="e9aab-150">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="e9aab-150">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aab-151">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e9aab-151">-InformationVariable</span></span>
<span data-ttu-id="e9aab-152">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="e9aab-152">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aab-153">-Przygotuj</span><span class="sxs-lookup"><span data-stu-id="e9aab-153">-Prepare</span></span>
<span data-ttu-id="e9aab-154">Wskazuje, że to polecenie cmdlet przygotowuje usługę w chmurze do migracji.</span><span class="sxs-lookup"><span data-stu-id="e9aab-154">Indicates that this cmdlet prepares the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, PrepareExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aab-155">-Profile</span><span class="sxs-lookup"><span data-stu-id="e9aab-155">-Profile</span></span>
<span data-ttu-id="e9aab-156">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9aab-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e9aab-157">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e9aab-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aab-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e9aab-158">-ServiceName</span></span>
<span data-ttu-id="e9aab-159">Określa nazwę usługi w chmurze, którą to polecenie cmdlet migruje.</span><span class="sxs-lookup"><span data-stu-id="e9aab-159">Specifies the name  of the cloud service that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9aab-160">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="e9aab-160">-SubnetName</span></span>
<span data-ttu-id="e9aab-161">Określa nazwę podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e9aab-161">Specifies the name of the Subnet inside the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aab-162">-UseExistingVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e9aab-162">-UseExistingVirtualNetwork</span></span>
<span data-ttu-id="e9aab-163">Wskazuje, że to polecenie cmdlet migruje usługę w chmurze do istniejącej sieci wirtualnej na stosie usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="e9aab-163">Indicates that this cmdlet migrates the cloud service to an existing virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aab-164">-Validate</span><span class="sxs-lookup"><span data-stu-id="e9aab-164">-Validate</span></span>
<span data-ttu-id="e9aab-165">Określa, że to polecenie cmdlet sprawdza poprawność usługi w chmurze do migracji.</span><span class="sxs-lookup"><span data-stu-id="e9aab-165">Specifies that this cmdlet validates the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateNewMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aab-166">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e9aab-166">-VirtualNetworkName</span></span>
<span data-ttu-id="e9aab-167">Określa nazwę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e9aab-167">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aab-168">-VirtualNetworkResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9aab-168">-VirtualNetworkResourceGroupName</span></span>
<span data-ttu-id="e9aab-169">Określa nazwę grupy zasobów istniejącej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e9aab-169">Specifies the name of the resource group of an existing virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aab-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9aab-170">CommonParameters</span></span>
<span data-ttu-id="e9aab-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9aab-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9aab-172">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9aab-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9aab-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9aab-173">INPUTS</span></span>

## <span data-ttu-id="e9aab-174">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9aab-174">OUTPUTS</span></span>

## <span data-ttu-id="e9aab-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9aab-175">NOTES</span></span>

## <span data-ttu-id="e9aab-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9aab-176">RELATED LINKS</span></span>

[<span data-ttu-id="e9aab-177">Przenieś — AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e9aab-177">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="e9aab-178">Przenieś — AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="e9aab-178">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="e9aab-179">Przenieś — AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="e9aab-179">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="e9aab-180">Przenieś — AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9aab-180">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="e9aab-181">Przenieś — AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e9aab-181">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


