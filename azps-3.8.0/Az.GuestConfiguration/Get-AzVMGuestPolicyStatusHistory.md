---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050118"
---
# <span data-ttu-id="155db-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="155db-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="155db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="155db-102">SYNOPSIS</span></span>
<span data-ttu-id="155db-103">Pobiera historię stanu zgodności zasad konfiguracji gościa dla inicjatywy typu "Gość konfiguracja" przypisaną do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="155db-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="155db-104">Inicjatywa to zasada typu definicji "Inicjatywa".</span><span class="sxs-lookup"><span data-stu-id="155db-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="155db-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="155db-105">SYNTAX</span></span>

### <span data-ttu-id="155db-106">InitiativeNameScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="155db-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="155db-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="155db-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="155db-108">Opis</span><span class="sxs-lookup"><span data-stu-id="155db-108">DESCRIPTION</span></span>
<span data-ttu-id="155db-109">Polecenie cmdlet Get-AzVMGuestPolicyStatusHistory pobiera historię stanu zgodności zasad konfiguracji Gości z inicjatywy typu "Gość konfiguracja" przypisaną do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="155db-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="155db-110">Inicjatywa to zasada typu definicji "Inicjatywa".</span><span class="sxs-lookup"><span data-stu-id="155db-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="155db-111">Użyj polecenia cmdlet Get-AzVMGuestPolicyStatus, aby uzyskać szczegółowe informacje o pojedynczym stanie zgodności przy użyciu ReportId, który można znaleźć w wynikach Get-AzVMGuestPolicyStatusHistory polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="155db-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="155db-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="155db-112">EXAMPLES</span></span>

### <span data-ttu-id="155db-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="155db-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="155db-114">Pobiera historię stanu zgodności według identyfikatora inicjatywy. ShowOnlyChange Switch wyświetla tylko zmiany stanu historycznego.</span><span class="sxs-lookup"><span data-stu-id="155db-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="155db-115">Pomija Stany, które nie zmieniły się między dwoma sprawdzeniami zgodności.</span><span class="sxs-lookup"><span data-stu-id="155db-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="155db-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="155db-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="155db-117">Pobiera historię stanu zgodności według nazwy inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="155db-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="155db-118">W przełączniku ShowOnlyChange są wyświetlane tylko zmiany stanu historycznego.</span><span class="sxs-lookup"><span data-stu-id="155db-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="155db-119">Pomija Stany, które nie zmieniły się między dwoma sprawdzeniami zgodności.</span><span class="sxs-lookup"><span data-stu-id="155db-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="155db-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="155db-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="155db-121">Pobiera historię stanu zgodności dla wszystkich zasad konfiguracji gościa przypisanych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="155db-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="155db-122">W przełączniku ShowOnlyChange są wyświetlane tylko zmiany stanu historycznego.</span><span class="sxs-lookup"><span data-stu-id="155db-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="155db-123">Pomija Stany, które nie zmieniły się między dwoma sprawdzeniami zgodności.</span><span class="sxs-lookup"><span data-stu-id="155db-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="155db-124">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="155db-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="155db-125">Pobiera historię stanu zgodności według identyfikatora inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="155db-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="155db-126">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="155db-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="155db-127">Pobiera historię stanu zgodności według nazwy inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="155db-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="155db-128">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="155db-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="155db-129">Pobiera historię stanu zgodności dla wszystkich zasad konfiguracji gościa przypisanych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="155db-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="155db-130">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="155db-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="155db-131">Stan zasad konfiguracji gościa jest wyświetlany według ReportId.</span><span class="sxs-lookup"><span data-stu-id="155db-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="155db-132">ReportId jest właściwością ReportId, którą można znaleźć w wynikach funkcji Get-AzVMGuestPolicyStatusHistory.</span><span class="sxs-lookup"><span data-stu-id="155db-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="155db-133">(Zobacz inne przykłady)</span><span class="sxs-lookup"><span data-stu-id="155db-133">(please refer other examples)</span></span>

## <span data-ttu-id="155db-134">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="155db-134">PARAMETERS</span></span>

### <span data-ttu-id="155db-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="155db-135">-DefaultProfile</span></span>
<span data-ttu-id="155db-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="155db-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="155db-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="155db-137">-InitiativeId</span></span>
<span data-ttu-id="155db-138">Identyfikator definicji zasady, w której typ definicji to inicjatywa, a kategoria to konfiguracja gościa</span><span class="sxs-lookup"><span data-stu-id="155db-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="155db-139">-Initiativename</span><span class="sxs-lookup"><span data-stu-id="155db-139">-InitiativeName</span></span>
<span data-ttu-id="155db-140">Nazwa zasady, w której typ definicji to inicjatywa, a kategoria to konfiguracja gościa</span><span class="sxs-lookup"><span data-stu-id="155db-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="155db-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="155db-141">-ResourceGroupName</span></span>
<span data-ttu-id="155db-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="155db-142">Resource group name.</span></span>

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

### <span data-ttu-id="155db-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="155db-143">-ShowOnlyChange</span></span>
<span data-ttu-id="155db-144">Umożliwia wyświetlanie zmian stanu historycznego tylko dla zasad konfiguracji gościa.</span><span class="sxs-lookup"><span data-stu-id="155db-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="155db-145">Pomija Stany, które nie zmieniły się między dwoma uruchomieniami inspekcji stanu zgodności.</span><span class="sxs-lookup"><span data-stu-id="155db-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

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

### <span data-ttu-id="155db-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="155db-146">-VMName</span></span>
<span data-ttu-id="155db-147">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="155db-147">VM name.</span></span>

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

### <span data-ttu-id="155db-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="155db-148">CommonParameters</span></span>
<span data-ttu-id="155db-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="155db-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="155db-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="155db-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="155db-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="155db-151">INPUTS</span></span>

### <span data-ttu-id="155db-152">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="155db-152">None</span></span>
## <span data-ttu-id="155db-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="155db-153">OUTPUTS</span></span>

### <span data-ttu-id="155db-154">Microsoft. Azure. Commands. GuestConfiguration. models. PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="155db-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="155db-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="155db-155">NOTES</span></span>

## <span data-ttu-id="155db-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="155db-156">RELATED LINKS</span></span>
