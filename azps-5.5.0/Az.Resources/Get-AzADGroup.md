---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 764b2d091b0019cc4231828066b4067c5f054476
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178906"
---
# <span data-ttu-id="38656-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="38656-101">Get-AzADGroup</span></span>

## <span data-ttu-id="38656-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38656-102">SYNOPSIS</span></span>
<span data-ttu-id="38656-103">Filtruje grupy usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="38656-103">Filters active directory groups.</span></span>

## <span data-ttu-id="38656-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="38656-104">SYNTAX</span></span>

### <span data-ttu-id="38656-105">EmptyParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="38656-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="38656-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="38656-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="38656-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="38656-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="38656-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38656-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="38656-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="38656-109">DESCRIPTION</span></span>
<span data-ttu-id="38656-110">Filtruje grupy usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="38656-110">Filters active directory groups.</span></span>

## <span data-ttu-id="38656-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="38656-111">EXAMPLES</span></span>

### <span data-ttu-id="38656-112">Przykład 1. Lista wszystkich grup usługi AD</span><span class="sxs-lookup"><span data-stu-id="38656-112">Example 1: List all AD groups</span></span>
```powershell
PS C:\> Get-AzADGroup
```

<span data-ttu-id="38656-113">Lista wszystkich grup usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="38656-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="38656-114">Przykład 2. Lista wszystkich grup usługi AD przy użyciu stronicowania</span><span class="sxs-lookup"><span data-stu-id="38656-114">Example 2: List all AD groups using paging</span></span>

```powershell
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="38656-115">Wyświetla listę pierwszych 100 grup usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="38656-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="38656-116">Przykład 3. Uzyskiwanie grupy usługi AD według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="38656-116">Example 3: Get AD group by object id</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="38656-117">Pobiera grupę usługi AD o identyfikatorze obiektu '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="38656-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="38656-118">Przykład 4. Lista grup według ciągu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="38656-118">Example 4: List groups by search string</span></span>

```powershell
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="38656-119">Lista wszystkich grup usługi AD, których nazwa wyświetlana zaczyna się od "Jan".</span><span class="sxs-lookup"><span data-stu-id="38656-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="38656-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38656-120">PARAMETERS</span></span>

### <span data-ttu-id="38656-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38656-121">-DefaultProfile</span></span>
<span data-ttu-id="38656-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="38656-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38656-123">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="38656-123">-DisplayName</span></span>
<span data-ttu-id="38656-124">Nazwa wyświetlana grupy.</span><span class="sxs-lookup"><span data-stu-id="38656-124">The display name of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38656-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="38656-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="38656-126">Służy do wyszukiwania grup, które zaczynają się od podanego ciągu.</span><span class="sxs-lookup"><span data-stu-id="38656-126">Used to find groups that begin with the provided string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38656-127">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="38656-127">-ObjectId</span></span>
<span data-ttu-id="38656-128">Identyfikator obiektu grupy.</span><span class="sxs-lookup"><span data-stu-id="38656-128">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38656-129">- IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="38656-129">-IncludeTotalCount</span></span>
<span data-ttu-id="38656-130">Raportuje liczbę obiektów w zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="38656-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="38656-131">Obecnie ten parametr nie działa nic.</span><span class="sxs-lookup"><span data-stu-id="38656-131">Currently, this parameter does nothing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38656-132">— Pomiń</span><span class="sxs-lookup"><span data-stu-id="38656-132">-Skip</span></span>
<span data-ttu-id="38656-133">Ignoruje pierwsze obiekty N, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="38656-133">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38656-134">— Najpierw</span><span class="sxs-lookup"><span data-stu-id="38656-134">-First</span></span>
<span data-ttu-id="38656-135">Maksymalna liczba obiektów, które mają być zwracane.</span><span class="sxs-lookup"><span data-stu-id="38656-135">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38656-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38656-136">CommonParameters</span></span>
<span data-ttu-id="38656-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38656-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38656-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38656-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38656-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38656-139">INPUTS</span></span>

### <span data-ttu-id="38656-140">System.String</span><span class="sxs-lookup"><span data-stu-id="38656-140">System.String</span></span>

### <span data-ttu-id="38656-141">System.Guid</span><span class="sxs-lookup"><span data-stu-id="38656-141">System.Guid</span></span>

## <span data-ttu-id="38656-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="38656-142">OUTPUTS</span></span>

### <span data-ttu-id="38656-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="38656-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="38656-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="38656-144">NOTES</span></span>

## <span data-ttu-id="38656-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38656-145">RELATED LINKS</span></span>

[<span data-ttu-id="38656-146">Get-AzadUser</span><span class="sxs-lookup"><span data-stu-id="38656-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="38656-147">Get-AzadServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="38656-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="38656-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="38656-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

