---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237789"
---
# <span data-ttu-id="0cf6d-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="0cf6d-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="0cf6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cf6d-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf6d-103">Pobiera historię stanu zgodności zasad konfiguracji gościa dla inicjatywy typu "Konfiguracja gościa" przypisanej do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="0cf6d-104">Inicjatywy to zasady typu definicji "Inicjatywy".</span><span class="sxs-lookup"><span data-stu-id="0cf6d-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="0cf6d-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0cf6d-105">SYNTAX</span></span>

### <span data-ttu-id="0cf6d-106">InitiativeNameScope (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="0cf6d-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cf6d-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="0cf6d-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cf6d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0cf6d-108">DESCRIPTION</span></span>
<span data-ttu-id="0cf6d-109">Polecenie Get-AzVMGuestPolicyStatusHistory cmdlet pobiera historię stanu zgodności zasad konfiguracji gościa dla inicjatywy typu "Konfiguracja gościa" przypisanej do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="0cf6d-110">Inicjatywy to zasady typu definicji "Inicjatywy".</span><span class="sxs-lookup"><span data-stu-id="0cf6d-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="0cf6d-111">Użyj Get-AzVMGuestPolicyStatus cmdlet, aby uzyskać szczegółowe informacje o pojedynczym stanie zgodności przy użyciu funkcji ReportId, które można znaleźć w wynikach Get-AzVMGuestPolicyStatusHistory cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="0cf6d-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0cf6d-112">EXAMPLES</span></span>

### <span data-ttu-id="0cf6d-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0cf6d-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="0cf6d-114">Pobiera historię stanu zgodności według identyfikatora inicjatywy. Przełącznik ShowOnlyChange pokazuje tylko historyczne zmiany stanu.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="0cf6d-115">Pomija stany, które nie zmieniły się między dwoma testami zgodności.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="0cf6d-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0cf6d-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="0cf6d-117">Pobiera historię stanu zgodności według nazwy inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="0cf6d-118">Przełącznik ShowOnlyChange pokazuje tylko zmiany stanu historycznego.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="0cf6d-119">Pomija stany, które nie zmieniły się między dwoma testami zgodności.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="0cf6d-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0cf6d-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="0cf6d-121">Pobiera historię stanu zgodności dla wszystkich zasad konfiguracji gościa przypisanych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="0cf6d-122">Przełącznik ShowOnlyChange pokazuje tylko zmiany stanu historycznego.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="0cf6d-123">Pomija stany, które nie zmieniły się między dwoma testami zgodności.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="0cf6d-124">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="0cf6d-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="0cf6d-125">Pobiera historię stanu zgodności według identyfikatora inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="0cf6d-126">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="0cf6d-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="0cf6d-127">Pobiera historię stanu zgodności według nazwy inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="0cf6d-128">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="0cf6d-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="0cf6d-129">Pobiera historię stanu zgodności dla wszystkich zasad konfiguracji gościa przypisanych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="0cf6d-130">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="0cf6d-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="0cf6d-131">Uzyskaj stan zasad konfiguracji gościa według raportu ReportId.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="0cf6d-132">ReportId to właściwość ReportId, która znajduje się w wynikach właściwości Get-AzVMGuestPolicyStatusHistory.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="0cf6d-133">(zapoznaj się z innymi przykładami)</span><span class="sxs-lookup"><span data-stu-id="0cf6d-133">(please refer other examples)</span></span>

## <span data-ttu-id="0cf6d-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cf6d-134">PARAMETERS</span></span>

### <span data-ttu-id="0cf6d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf6d-135">-DefaultProfile</span></span>
<span data-ttu-id="0cf6d-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cf6d-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="0cf6d-137">-InitiativeId</span></span>
<span data-ttu-id="0cf6d-138">Identyfikator definicji zasad, w których typem definicji jest Initiative, a kategorią jest konfiguracja gościa</span><span class="sxs-lookup"><span data-stu-id="0cf6d-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf6d-139">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="0cf6d-139">-InitiativeName</span></span>
<span data-ttu-id="0cf6d-140">Nazwa zasad, w których typem definicji jest Initiative, a kategorią jest Konfiguracja gościa</span><span class="sxs-lookup"><span data-stu-id="0cf6d-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="0cf6d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cf6d-141">-ResourceGroupName</span></span>
<span data-ttu-id="0cf6d-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-142">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf6d-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="0cf6d-143">-ShowOnlyChange</span></span>
<span data-ttu-id="0cf6d-144">Pokazuje historyczne zmiany stanu tylko w przypadku zasad konfiguracji gościa.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="0cf6d-145">Pomija stany, które nie zmieniły się między dwoma inspekcjami stanu zgodności.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf6d-146">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="0cf6d-146">-VMName</span></span>
<span data-ttu-id="0cf6d-147">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-147">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf6d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf6d-148">CommonParameters</span></span>
<span data-ttu-id="0cf6d-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cf6d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf6d-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cf6d-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf6d-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cf6d-151">INPUTS</span></span>

### <span data-ttu-id="0cf6d-152">Brak</span><span class="sxs-lookup"><span data-stu-id="0cf6d-152">None</span></span>
## <span data-ttu-id="0cf6d-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cf6d-153">OUTPUTS</span></span>

### <span data-ttu-id="0cf6d-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="0cf6d-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="0cf6d-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0cf6d-155">NOTES</span></span>

## <span data-ttu-id="0cf6d-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0cf6d-156">RELATED LINKS</span></span>
