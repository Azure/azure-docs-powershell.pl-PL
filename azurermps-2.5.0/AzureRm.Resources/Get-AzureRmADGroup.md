---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
ms.openlocfilehash: 9ddc9658d6d18cc7a08df33f1f976521656c9234
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898205"
---
# <span data-ttu-id="cf1bf-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="cf1bf-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="cf1bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf1bf-102">SYNOPSIS</span></span>
<span data-ttu-id="cf1bf-103">Umożliwia filtrowanie grup usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cf1bf-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf1bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf1bf-104">SYNTAX</span></span>

### <span data-ttu-id="cf1bf-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cf1bf-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cf1bf-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf1bf-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cf1bf-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf1bf-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cf1bf-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf1bf-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="cf1bf-109">Opis</span><span class="sxs-lookup"><span data-stu-id="cf1bf-109">DESCRIPTION</span></span>
<span data-ttu-id="cf1bf-110">Umożliwia filtrowanie grup usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cf1bf-110">Filters active directory groups.</span></span>

## <span data-ttu-id="cf1bf-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf1bf-111">EXAMPLES</span></span>

### <span data-ttu-id="cf1bf-112">Przykład 1-Lista wszystkich grup usługi AD</span><span class="sxs-lookup"><span data-stu-id="cf1bf-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="cf1bf-113">Lista wszystkich grup usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="cf1bf-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="cf1bf-114">Przykład 2-Wyświetlanie listy wszystkich grup usługi AD za pomocą stronicowania</span><span class="sxs-lookup"><span data-stu-id="cf1bf-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzureRmADGroup -First 100
```

<span data-ttu-id="cf1bf-115">Lista pierwszych 100 grup usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="cf1bf-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="cf1bf-116">Przykład 3 — Uzyskaj grupę AD według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="cf1bf-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="cf1bf-117">Pobiera grupę usługi AD o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="cf1bf-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="cf1bf-118">Przykład 4-wyświetlanie grup według ciągu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="cf1bf-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="cf1bf-119">Wyświetla listę wszystkich grup usługi AD, których nazwa wyświetlana zaczyna się od ciągu "Janusz".</span><span class="sxs-lookup"><span data-stu-id="cf1bf-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="cf1bf-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf1bf-120">PARAMETERS</span></span>

### <span data-ttu-id="cf1bf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf1bf-121">-DefaultProfile</span></span>
<span data-ttu-id="cf1bf-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cf1bf-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf1bf-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cf1bf-123">-DisplayName</span></span>
<span data-ttu-id="cf1bf-124">Nazwa wyświetlana grupy.</span><span class="sxs-lookup"><span data-stu-id="cf1bf-124">The display name of the group.</span></span>

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

### <span data-ttu-id="cf1bf-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="cf1bf-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="cf1bf-126">Służy do znajdowania grup zaczynających się od podanego ciągu.</span><span class="sxs-lookup"><span data-stu-id="cf1bf-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="cf1bf-127">-First</span><span class="sxs-lookup"><span data-stu-id="cf1bf-127">-First</span></span>
<span data-ttu-id="cf1bf-128">Maksymalna liczba obiektów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="cf1bf-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="cf1bf-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="cf1bf-129">-IncludeTotalCount</span></span>
<span data-ttu-id="cf1bf-130">Wyświetla liczbę obiektów w zbiorze danych.</span><span class="sxs-lookup"><span data-stu-id="cf1bf-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="cf1bf-131">Obecnie ten parametr nie wykonuje żadnych działań.</span><span class="sxs-lookup"><span data-stu-id="cf1bf-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="cf1bf-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cf1bf-132">-ObjectId</span></span>
<span data-ttu-id="cf1bf-133">Identyfikator obiektu grupy.</span><span class="sxs-lookup"><span data-stu-id="cf1bf-133">Object id of the group.</span></span>

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

### <span data-ttu-id="cf1bf-134">-Skip</span><span class="sxs-lookup"><span data-stu-id="cf1bf-134">-Skip</span></span>
<span data-ttu-id="cf1bf-135">Ignoruje pierwsze N obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="cf1bf-135">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="cf1bf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf1bf-136">CommonParameters</span></span>
<span data-ttu-id="cf1bf-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf1bf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf1bf-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf1bf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf1bf-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf1bf-139">INPUTS</span></span>

### <span data-ttu-id="cf1bf-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cf1bf-140">System.String</span></span>

### <span data-ttu-id="cf1bf-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="cf1bf-141">System.Guid</span></span>

## <span data-ttu-id="cf1bf-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf1bf-142">OUTPUTS</span></span>

### <span data-ttu-id="cf1bf-143">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="cf1bf-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="cf1bf-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf1bf-144">NOTES</span></span>

## <span data-ttu-id="cf1bf-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf1bf-145">RELATED LINKS</span></span>

[<span data-ttu-id="cf1bf-146">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="cf1bf-146">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="cf1bf-147">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cf1bf-147">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="cf1bf-148">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="cf1bf-148">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

