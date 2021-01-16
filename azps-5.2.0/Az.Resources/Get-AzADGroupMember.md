---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: 984b5ef9a1ff19142ef044e1f3c919f8fb2a3dce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366023"
---
# <span data-ttu-id="641d7-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="641d7-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="641d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="641d7-102">SYNOPSIS</span></span>
<span data-ttu-id="641d7-103">Wyświetla listę członków grupy usługi AD w bieżącej dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="641d7-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="641d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="641d7-104">SYNTAX</span></span>

### <span data-ttu-id="641d7-105">ObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="641d7-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="641d7-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="641d7-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="641d7-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="641d7-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="641d7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="641d7-108">DESCRIPTION</span></span>
<span data-ttu-id="641d7-109">Wyświetla listę członków grupy usługi AD w bieżącej dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="641d7-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="641d7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="641d7-110">EXAMPLES</span></span>

### <span data-ttu-id="641d7-111">Przykład 1: wyświetlanie członków listy według identyfikatora obiektu grupy usługi AD</span><span class="sxs-lookup"><span data-stu-id="641d7-111">Example 1: List members by AD group object id</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="641d7-112">Wyświetla listę członków grupy usługi AD o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="641d7-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="641d7-113">Przykład 2: Wyświetlanie listy członków według identyfikatora obiektu grupy usługi AD za pomocą stronicowania</span><span class="sxs-lookup"><span data-stu-id="641d7-113">Example 2: List members by AD group object id using paging</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="641d7-114">Wyświetla listę pierwszych 100 członków grupy usługi AD o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="641d7-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="641d7-115">Przykład 3: Wyświetlanie listy członków według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="641d7-115">Example 3: List members by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="641d7-116">Pobiera grupę usługi AD o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE" i przekazuje ją do polecenia cmdlet Get-AzADGroupMember, aby wyświetlić listę wszystkich członków tej grupy.</span><span class="sxs-lookup"><span data-stu-id="641d7-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="641d7-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="641d7-117">PARAMETERS</span></span>

### <span data-ttu-id="641d7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="641d7-118">-DefaultProfile</span></span>
<span data-ttu-id="641d7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="641d7-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="641d7-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="641d7-120">-GroupDisplayName</span></span>
<span data-ttu-id="641d7-121">Nazwa wyświetlana grupy.</span><span class="sxs-lookup"><span data-stu-id="641d7-121">The display name of the group.</span></span>

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

### <span data-ttu-id="641d7-122">-Groupobject</span><span class="sxs-lookup"><span data-stu-id="641d7-122">-GroupObject</span></span>
<span data-ttu-id="641d7-123">Obiekt grupy, z którego będą wymieniani członkowie.</span><span class="sxs-lookup"><span data-stu-id="641d7-123">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="641d7-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="641d7-124">-GroupObjectId</span></span>
<span data-ttu-id="641d7-125">Identyfikator obiektu grupy.</span><span class="sxs-lookup"><span data-stu-id="641d7-125">Object Id of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="641d7-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="641d7-126">-IncludeTotalCount</span></span>
<span data-ttu-id="641d7-127">Wyświetla liczbę obiektów w zbiorze danych.</span><span class="sxs-lookup"><span data-stu-id="641d7-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="641d7-128">Obecnie ten parametr nie wykonuje żadnych działań.</span><span class="sxs-lookup"><span data-stu-id="641d7-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="641d7-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="641d7-129">-Skip</span></span>
<span data-ttu-id="641d7-130">Ignoruje pierwsze N obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="641d7-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="641d7-131">-First</span><span class="sxs-lookup"><span data-stu-id="641d7-131">-First</span></span>
<span data-ttu-id="641d7-132">Maksymalna liczba obiektów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="641d7-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="641d7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="641d7-133">CommonParameters</span></span>
<span data-ttu-id="641d7-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="641d7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="641d7-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="641d7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="641d7-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="641d7-136">INPUTS</span></span>

### <span data-ttu-id="641d7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="641d7-137">System.String</span></span>

### <span data-ttu-id="641d7-138">Microsoft. Azure. Commands. pozycji. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="641d7-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="641d7-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="641d7-139">OUTPUTS</span></span>

### <span data-ttu-id="641d7-140">Microsoft. Azure. Commands. pozycji. PSADObject</span><span class="sxs-lookup"><span data-stu-id="641d7-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="641d7-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="641d7-141">NOTES</span></span>

## <span data-ttu-id="641d7-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="641d7-142">RELATED LINKS</span></span>

[<span data-ttu-id="641d7-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="641d7-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="641d7-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="641d7-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

