---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: ffc04a6b1560845a0c29db4d000270fe91aa8ff4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554258"
---
# <span data-ttu-id="363f9-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="363f9-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="363f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="363f9-102">SYNOPSIS</span></span>
<span data-ttu-id="363f9-103">Wyświetla listę członków grupy usługi AD w bieżącej dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="363f9-103">Lists members of an AD group in the current tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="363f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="363f9-104">SYNTAX</span></span>

### <span data-ttu-id="363f9-105">ObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="363f9-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="363f9-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="363f9-106">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="363f9-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="363f9-107">GroupObjectParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="363f9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="363f9-108">DESCRIPTION</span></span>
<span data-ttu-id="363f9-109">Wyświetla listę członków grupy usługi AD w bieżącej dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="363f9-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="363f9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="363f9-110">EXAMPLES</span></span>

### <span data-ttu-id="363f9-111">Przykład 1-Wyświetlanie członków listy według identyfikatora obiektu grupy usługi AD</span><span class="sxs-lookup"><span data-stu-id="363f9-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="363f9-112">Wyświetla listę członków grupy usługi AD o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="363f9-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="363f9-113">Przykład 2-Wyświetlanie listy członków według identyfikatora obiektu grupy usługi AD przy użyciu stronicowania</span><span class="sxs-lookup"><span data-stu-id="363f9-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="363f9-114">Wyświetla listę pierwszych 100 członków grupy usługi AD o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="363f9-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="363f9-115">Przykład 3-wyświetla listę członków według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="363f9-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzureRmADGroupMember
```

<span data-ttu-id="363f9-116">Pobiera grupę usługi AD o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE" i przekazuje ją do polecenia cmdlet Get-AzureRmADGroupMember, aby wyświetlić listę wszystkich członków tej grupy.</span><span class="sxs-lookup"><span data-stu-id="363f9-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzureRmADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="363f9-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="363f9-117">PARAMETERS</span></span>

### <span data-ttu-id="363f9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="363f9-118">-DefaultProfile</span></span>
<span data-ttu-id="363f9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="363f9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="363f9-120">-First</span><span class="sxs-lookup"><span data-stu-id="363f9-120">-First</span></span>
<span data-ttu-id="363f9-121">Maksymalna liczba obiektów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="363f9-121">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="363f9-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="363f9-122">-GroupDisplayName</span></span>
<span data-ttu-id="363f9-123">Nazwa wyświetlana grupy.</span><span class="sxs-lookup"><span data-stu-id="363f9-123">The display name of the group.</span></span>

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

### <span data-ttu-id="363f9-124">-Groupobject</span><span class="sxs-lookup"><span data-stu-id="363f9-124">-GroupObject</span></span>
<span data-ttu-id="363f9-125">Obiekt grupy, z którego będą wymieniani członkowie.</span><span class="sxs-lookup"><span data-stu-id="363f9-125">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="363f9-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="363f9-126">-GroupObjectId</span></span>
<span data-ttu-id="363f9-127">Identyfikator obiektu grupy.</span><span class="sxs-lookup"><span data-stu-id="363f9-127">Object Id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="363f9-128">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="363f9-128">-IncludeTotalCount</span></span>
<span data-ttu-id="363f9-129">Wyświetla liczbę obiektów w zbiorze danych.</span><span class="sxs-lookup"><span data-stu-id="363f9-129">Reports the number of objects in the data set.</span></span> <span data-ttu-id="363f9-130">Obecnie ten parametr nie wykonuje żadnych działań.</span><span class="sxs-lookup"><span data-stu-id="363f9-130">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="363f9-131">-Skip</span><span class="sxs-lookup"><span data-stu-id="363f9-131">-Skip</span></span>
<span data-ttu-id="363f9-132">Ignoruje pierwsze N obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="363f9-132">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="363f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="363f9-133">CommonParameters</span></span>
<span data-ttu-id="363f9-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="363f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="363f9-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="363f9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="363f9-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="363f9-136">INPUTS</span></span>

### <span data-ttu-id="363f9-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="363f9-137">System.Guid</span></span>

### <span data-ttu-id="363f9-138">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="363f9-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="363f9-139">Parametry: Groupobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="363f9-139">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="363f9-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="363f9-140">OUTPUTS</span></span>

### <span data-ttu-id="363f9-141">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADObject</span><span class="sxs-lookup"><span data-stu-id="363f9-141">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="363f9-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="363f9-142">NOTES</span></span>

## <span data-ttu-id="363f9-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="363f9-143">RELATED LINKS</span></span>

[<span data-ttu-id="363f9-144">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="363f9-144">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="363f9-145">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="363f9-145">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

