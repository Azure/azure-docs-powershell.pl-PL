---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: c1bf608c76c547360d9d7a48f4ba74c1713ee049
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705354"
---
# <span data-ttu-id="39547-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="39547-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="39547-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39547-102">SYNOPSIS</span></span>
<span data-ttu-id="39547-103">Pobiera stan zasad konfiguracji gościa (szczegółowy) z inicjatywy typu "Gość konfiguracja" przypisanej do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="39547-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="39547-104">Inicjatywa to zasada typu definicji "Inicjatywa".</span><span class="sxs-lookup"><span data-stu-id="39547-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="39547-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39547-105">SYNTAX</span></span>

### <span data-ttu-id="39547-106">VmScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="39547-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39547-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="39547-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39547-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="39547-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39547-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="39547-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39547-110">Opis</span><span class="sxs-lookup"><span data-stu-id="39547-110">DESCRIPTION</span></span>
<span data-ttu-id="39547-111">Polecenie cmdlet Get-AzVMGuestPolicyStatus umożliwia pobieranie stanu zasad konfiguracji Gościa z inicjatywy typu "Gość konfiguracja" przypisanej do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="39547-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="39547-112">Inicjatywa to zasada typu definicji "Inicjatywa".</span><span class="sxs-lookup"><span data-stu-id="39547-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="39547-113">To polecenie cmdlet pobiera stan zgodności maszyny wirtualnej oraz powody, dla których nie jest on zgodny z indywidualnymi zasadami z inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="39547-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="39547-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39547-114">EXAMPLES</span></span>

### <span data-ttu-id="39547-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="39547-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="39547-116">Uzyskaj wszystkie najnowsze Stany zasad konfiguracji Gości dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="39547-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="39547-117">Stan obejmuje stan zgodności maszyny wirtualnej dla każdej zasady we wszystkich inicjatywach typu "Konfiguracja gościa", przyczyny zgodności, czas sprawdzania zgodności, informacje o zasobach, które sprawdziły się pod kątem zgodności.</span><span class="sxs-lookup"><span data-stu-id="39547-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="39547-118">Wyniki zawierają najnowsze Stany, nie obejmuje wcześniejszych stanów historycznych.</span><span class="sxs-lookup"><span data-stu-id="39547-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="39547-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="39547-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="39547-120">Uzyskaj najnowsze Stany zasad konfiguracji gościa według identyfikatora inicjatywy. Stan obejmuje stan zgodności maszyny wirtualnej dla każdej zasady z inicjatywy, przyczyn zgodności, czasu sprawdzania zgodności, informacji o zasobie, które sprawdziły się pod kątem zgodności.</span><span class="sxs-lookup"><span data-stu-id="39547-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="39547-121">Wyniki nie uwzględniają wcześniejszych wygenerowanych Stanów, ale zawiera najnowszy status dla każdej zasady z inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="39547-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="39547-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="39547-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="39547-123">Uzyskaj najnowsze Stany zasad konfiguracji gościa według nazwy inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="39547-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="39547-124">Stan obejmuje stan zgodności maszyny wirtualnej dla każdej zasady z inicjatywy, przyczyn zgodności, czasu sprawdzania zgodności, informacji o zasobie, które sprawdziły się pod kątem zgodności.</span><span class="sxs-lookup"><span data-stu-id="39547-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="39547-125">Wyniki nie uwzględniają wcześniejszych wygenerowanych Stanów, ale zawiera najnowszy status dla każdej zasady z inicjatywy.</span><span class="sxs-lookup"><span data-stu-id="39547-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="39547-126">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="39547-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="39547-127">Stan zasad konfiguracji gościa jest wyświetlany według ReportId.</span><span class="sxs-lookup"><span data-stu-id="39547-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="39547-128">ReportId jest właściwością ReportId, którą można znaleźć w wynikach Get-AzVMGuestPolicyStatus przy użyciu initiativeId lub nazwy inicjatywy (Proszę znaleźć inne przykłady).</span><span class="sxs-lookup"><span data-stu-id="39547-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="39547-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39547-129">PARAMETERS</span></span>

### <span data-ttu-id="39547-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39547-130">-DefaultProfile</span></span>
<span data-ttu-id="39547-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="39547-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39547-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="39547-132">-InitiativeId</span></span>
<span data-ttu-id="39547-133">Identyfikator definicji zasady, w której typ definicji to inicjatywa, a kategoria to konfiguracja gościa</span><span class="sxs-lookup"><span data-stu-id="39547-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="39547-134">-Initiativename</span><span class="sxs-lookup"><span data-stu-id="39547-134">-InitiativeName</span></span>
<span data-ttu-id="39547-135">Nazwa zasady, w której typ definicji to inicjatywa, a kategoria to konfiguracja gościa</span><span class="sxs-lookup"><span data-stu-id="39547-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="39547-136">-ReportId</span><span class="sxs-lookup"><span data-stu-id="39547-136">-ReportId</span></span>
<span data-ttu-id="39547-137">Identyfikator stanu zasad konfiguracji gościa.</span><span class="sxs-lookup"><span data-stu-id="39547-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="39547-138">Zasady, w których typ definicji to inicjatywa, a kategoria to konfiguracja gościa, musi być przypisana do zakresu w celu uzyskania statusu.</span><span class="sxs-lookup"><span data-stu-id="39547-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

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

### <span data-ttu-id="39547-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39547-139">-ResourceGroupName</span></span>
<span data-ttu-id="39547-140">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="39547-140">Resource group name.</span></span>

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

### <span data-ttu-id="39547-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="39547-141">-VMName</span></span>
<span data-ttu-id="39547-142">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="39547-142">VM name.</span></span>

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

### <span data-ttu-id="39547-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39547-143">CommonParameters</span></span>
<span data-ttu-id="39547-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39547-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39547-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39547-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39547-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39547-146">INPUTS</span></span>

### <span data-ttu-id="39547-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="39547-147">None</span></span>
## <span data-ttu-id="39547-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39547-148">OUTPUTS</span></span>

### <span data-ttu-id="39547-149">Microsoft. Azure. Commands. GuestConfiguration. models. PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="39547-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="39547-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39547-150">NOTES</span></span>

## <span data-ttu-id="39547-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39547-151">RELATED LINKS</span></span>