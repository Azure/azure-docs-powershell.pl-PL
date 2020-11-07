---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 8dc8188d9408c1b8e37fe44b149ceebeaf12ee4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544875"
---
# <span data-ttu-id="cc195-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="cc195-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="cc195-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc195-102">SYNOPSIS</span></span>
<span data-ttu-id="cc195-103">Umożliwia filtrowanie grup usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cc195-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc195-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc195-104">SYNTAX</span></span>

### <span data-ttu-id="cc195-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cc195-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cc195-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc195-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cc195-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc195-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cc195-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc195-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="cc195-109">Opis</span><span class="sxs-lookup"><span data-stu-id="cc195-109">DESCRIPTION</span></span>
<span data-ttu-id="cc195-110">Umożliwia filtrowanie grup usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cc195-110">Filters active directory groups.</span></span>

## <span data-ttu-id="cc195-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc195-111">EXAMPLES</span></span>

### <span data-ttu-id="cc195-112">Przykład 1-Lista wszystkich grup usługi AD</span><span class="sxs-lookup"><span data-stu-id="cc195-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="cc195-113">Lista wszystkich grup usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="cc195-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="cc195-114">Przykład 2-Wyświetlanie listy wszystkich grup usługi AD za pomocą stronicowania</span><span class="sxs-lookup"><span data-stu-id="cc195-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzureRmADGroup -First 100
```

<span data-ttu-id="cc195-115">Lista pierwszych 100 grup usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="cc195-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="cc195-116">Przykład 3 — Uzyskaj grupę AD według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="cc195-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="cc195-117">Pobiera grupę usługi AD o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="cc195-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="cc195-118">Przykład 4-wyświetlanie grup według ciągu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="cc195-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="cc195-119">Wyświetla listę wszystkich grup usługi AD, których nazwa wyświetlana zaczyna się od ciągu "Janusz".</span><span class="sxs-lookup"><span data-stu-id="cc195-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="cc195-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc195-120">PARAMETERS</span></span>

### <span data-ttu-id="cc195-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc195-121">-DefaultProfile</span></span>
<span data-ttu-id="cc195-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cc195-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc195-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cc195-123">-DisplayName</span></span>
<span data-ttu-id="cc195-124">Nazwa wyświetlana grupy.</span><span class="sxs-lookup"><span data-stu-id="cc195-124">The display name of the group.</span></span>

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

### <span data-ttu-id="cc195-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="cc195-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="cc195-126">Służy do znajdowania grup zaczynających się od podanego ciągu.</span><span class="sxs-lookup"><span data-stu-id="cc195-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="cc195-127">-First</span><span class="sxs-lookup"><span data-stu-id="cc195-127">-First</span></span>
<span data-ttu-id="cc195-128">Maksymalna liczba obiektów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="cc195-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="cc195-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="cc195-129">-IncludeTotalCount</span></span>
<span data-ttu-id="cc195-130">Wyświetla liczbę obiektów w zbiorze danych.</span><span class="sxs-lookup"><span data-stu-id="cc195-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="cc195-131">Obecnie ten parametr nie wykonuje żadnych działań.</span><span class="sxs-lookup"><span data-stu-id="cc195-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="cc195-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cc195-132">-ObjectId</span></span>
<span data-ttu-id="cc195-133">Identyfikator obiektu grupy.</span><span class="sxs-lookup"><span data-stu-id="cc195-133">Object id of the group.</span></span>

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

### <span data-ttu-id="cc195-134">-Skip</span><span class="sxs-lookup"><span data-stu-id="cc195-134">-Skip</span></span>
<span data-ttu-id="cc195-135">Ignoruje pierwsze N obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="cc195-135">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="cc195-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc195-136">CommonParameters</span></span>
<span data-ttu-id="cc195-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc195-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc195-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc195-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc195-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc195-139">INPUTS</span></span>

### <span data-ttu-id="cc195-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cc195-140">System.String</span></span>

### <span data-ttu-id="cc195-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="cc195-141">System.Guid</span></span>

## <span data-ttu-id="cc195-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc195-142">OUTPUTS</span></span>

### <span data-ttu-id="cc195-143">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="cc195-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="cc195-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc195-144">NOTES</span></span>

## <span data-ttu-id="cc195-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc195-145">RELATED LINKS</span></span>

[<span data-ttu-id="cc195-146">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="cc195-146">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="cc195-147">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cc195-147">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="cc195-148">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="cc195-148">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)
