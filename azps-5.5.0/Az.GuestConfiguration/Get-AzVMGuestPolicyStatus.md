---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187659"
---
# <span data-ttu-id="79e53-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="79e53-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="79e53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79e53-102">SYNOPSIS</span></span>
<span data-ttu-id="79e53-103">Pobiera stan zasad konfiguracji gościa (szczegółowy) dla inicjatywy typu "Konfiguracja gościa" przypisanej do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="79e53-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="79e53-104">Inicjatywy to zasady typu definicji "Inicjatywy".</span><span class="sxs-lookup"><span data-stu-id="79e53-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="79e53-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="79e53-105">SYNTAX</span></span>

### <span data-ttu-id="79e53-106">Żytoskop (domyślny)</span><span class="sxs-lookup"><span data-stu-id="79e53-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79e53-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="79e53-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79e53-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="79e53-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79e53-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="79e53-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79e53-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="79e53-110">DESCRIPTION</span></span>
<span data-ttu-id="79e53-111">Polecenie Get-AzVMGuestPolicyStatus pobiera stan zasad konfiguracji gościa dla inicjatywy typu "Konfiguracja gościa" przypisanej do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="79e53-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="79e53-112">Inicjatywy to zasady typu definicji "Inicjatywy".</span><span class="sxs-lookup"><span data-stu-id="79e53-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="79e53-113">To polecenie cmdlet otrzymuje stan zgodności maszyny wirtualnej i przyczyny, dla których jest ono niezgodne z poszczególnymi zasadami w ramach inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="79e53-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="79e53-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="79e53-114">EXAMPLES</span></span>

### <span data-ttu-id="79e53-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79e53-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="79e53-116">Uzyskaj wszystkie najnowsze statusy zasad konfiguracji gościa dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="79e53-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="79e53-117">Stan obejmuje stan zgodności maszyny wirtualnej dla każdej zasady we wszystkich inicjatywach typu "Konfiguracja gościa", powody zgodności, czas kontroli zgodności, informacje o zasobach sprawdzone pod kątem zgodności.</span><span class="sxs-lookup"><span data-stu-id="79e53-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="79e53-118">Wyniki zawierają najnowsze stany, ale nie zawierają poprzednich stanów historycznych.</span><span class="sxs-lookup"><span data-stu-id="79e53-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="79e53-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="79e53-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="79e53-120">Uzyskaj najnowsze statusy zasad konfiguracji gościa, korzystając z identyfikatora inicjatywy. Stan obejmuje stan zgodności maszyny wirtualnej dla każdej zasady w ramach inicjatywy, powody zgodności, czas sprawdzania zgodności, informacje o zasobach sprawdzone pod kątem zgodności.</span><span class="sxs-lookup"><span data-stu-id="79e53-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="79e53-121">Wyniki nie zawierają wygenerowanych poprzednich stanów, a jedynie najnowszy stan dla każdej zasady w ramach inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="79e53-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="79e53-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="79e53-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="79e53-123">Uzyskaj najnowsze statusy zasad konfiguracji gościa według nazwy inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="79e53-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="79e53-124">Stan obejmuje stan zgodności maszyny wirtualnej dla każdej zasady w ramach inicjatywy, powody zgodności, czas sprawdzania zgodności, informacje o zasobach sprawdzone pod kątem zgodności.</span><span class="sxs-lookup"><span data-stu-id="79e53-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="79e53-125">Wyniki nie zawierają wygenerowanych poprzednich stanów, a jedynie najnowszy stan dla każdej zasady w ramach inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="79e53-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="79e53-126">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="79e53-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="79e53-127">Uzyskaj stan zasad konfiguracji gościa według raportu ReportId.</span><span class="sxs-lookup"><span data-stu-id="79e53-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="79e53-128">ReportId to właściwość ReportId, która może zostać znaleziona w wynikach Get-AzVMGuestPolicyStatus initiativeId lub Initiative Name (zobacz inne przykłady)</span><span class="sxs-lookup"><span data-stu-id="79e53-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="79e53-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79e53-129">PARAMETERS</span></span>

### <span data-ttu-id="79e53-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e53-130">-DefaultProfile</span></span>
<span data-ttu-id="79e53-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="79e53-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79e53-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="79e53-132">-InitiativeId</span></span>
<span data-ttu-id="79e53-133">Identyfikator definicji zasad, w których typem definicji jest Initiative, a kategorią jest konfiguracja gościa</span><span class="sxs-lookup"><span data-stu-id="79e53-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e53-134">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="79e53-134">-InitiativeName</span></span>
<span data-ttu-id="79e53-135">Nazwa zasad, w których typem definicji jest Initiative, a kategorią jest Konfiguracja gościa</span><span class="sxs-lookup"><span data-stu-id="79e53-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e53-136">- ReportId</span><span class="sxs-lookup"><span data-stu-id="79e53-136">-ReportId</span></span>
<span data-ttu-id="79e53-137">Identyfikator stanu zasad konfiguracji gościa.</span><span class="sxs-lookup"><span data-stu-id="79e53-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="79e53-138">Zasady, w których typem definicji jest inicjatywa, a kategorią jest konfiguracja gościa, należy przypisać do zakresu, aby uzyskać statusy.</span><span class="sxs-lookup"><span data-stu-id="79e53-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e53-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79e53-139">-ResourceGroupName</span></span>
<span data-ttu-id="79e53-140">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="79e53-140">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e53-141">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="79e53-141">-VMName</span></span>
<span data-ttu-id="79e53-142">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="79e53-142">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e53-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e53-143">CommonParameters</span></span>
<span data-ttu-id="79e53-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79e53-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e53-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79e53-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e53-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79e53-146">INPUTS</span></span>

### <span data-ttu-id="79e53-147">Brak</span><span class="sxs-lookup"><span data-stu-id="79e53-147">None</span></span>
## <span data-ttu-id="79e53-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79e53-148">OUTPUTS</span></span>

### <span data-ttu-id="79e53-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="79e53-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="79e53-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="79e53-150">NOTES</span></span>

## <span data-ttu-id="79e53-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79e53-151">RELATED LINKS</span></span>
