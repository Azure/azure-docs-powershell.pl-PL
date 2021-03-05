---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 6f5ae29865775368427987dcfc1844c9235db593
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961690"
---
# <span data-ttu-id="32575-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="32575-101">Get-AzADUser</span></span>

## <span data-ttu-id="32575-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32575-102">SYNOPSIS</span></span>
<span data-ttu-id="32575-103">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="32575-103">Filters active directory users.</span></span>

## <span data-ttu-id="32575-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="32575-104">SYNTAX</span></span>

### <span data-ttu-id="32575-105">EmptyParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="32575-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="32575-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="32575-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="32575-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="32575-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="32575-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32575-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="32575-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="32575-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="32575-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="32575-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="32575-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="32575-111">DESCRIPTION</span></span>
<span data-ttu-id="32575-112">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="32575-112">Filters active directory users.</span></span>

## <span data-ttu-id="32575-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="32575-113">EXAMPLES</span></span>

### <span data-ttu-id="32575-114">Przykład 1. Lista wszystkich użytkowników</span><span class="sxs-lookup"><span data-stu-id="32575-114">Example 1: List all users</span></span>

```powershell
PS C:\> Get-AzADUser
```

<span data-ttu-id="32575-115">Wyświetla listę wszystkich użytkowników usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="32575-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="32575-116">Przykład 2. Lista wszystkich użytkowników używających stronicowania</span><span class="sxs-lookup"><span data-stu-id="32575-116">Example 2: List all users using paging</span></span>

```powershell
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="32575-117">Wyświetla listę pierwszych 100 użytkowników usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="32575-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="32575-118">Przykład 3. Uzyskiwanie użytkownika usługi AD według głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="32575-118">Example 3: Get AD user by user principal name</span></span>

```powershell
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="32575-119">Pobiera użytkownika usługi AD o głównej nazwie użytkownika" foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="32575-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="32575-120">Przykład 4. Lista według ciągu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="32575-120">Example 4: List by search string</span></span>

```powershell
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="32575-121">Wyświetla listę wszystkich użytkowników usługi AD, których nazwa wyświetlana zaczyna się od "Jan".</span><span class="sxs-lookup"><span data-stu-id="32575-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="32575-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32575-122">PARAMETERS</span></span>

### <span data-ttu-id="32575-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32575-123">-DefaultProfile</span></span>
<span data-ttu-id="32575-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="32575-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32575-125">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="32575-125">-DisplayName</span></span>
<span data-ttu-id="32575-126">Nazwa wyświetlana użytkownika.</span><span class="sxs-lookup"><span data-stu-id="32575-126">The display name of the user.</span></span>

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

### <span data-ttu-id="32575-127">— Poczta</span><span class="sxs-lookup"><span data-stu-id="32575-127">-Mail</span></span>
<span data-ttu-id="32575-128">Poczta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="32575-128">The user mail.</span></span>

```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32575-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="32575-129">-ObjectId</span></span>
<span data-ttu-id="32575-130">Identyfikator obiektu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="32575-130">Object id of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32575-131">—StartsWith</span><span class="sxs-lookup"><span data-stu-id="32575-131">-StartsWith</span></span>
<span data-ttu-id="32575-132">Umożliwia znalezienie użytkowników, którzy zaczynają się od podanego ciągu.</span><span class="sxs-lookup"><span data-stu-id="32575-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="32575-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="32575-133">-UserPrincipalName</span></span>
<span data-ttu-id="32575-134">UpN użytkownika.</span><span class="sxs-lookup"><span data-stu-id="32575-134">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32575-135">- IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="32575-135">-IncludeTotalCount</span></span>
<span data-ttu-id="32575-136">Raportuje liczbę obiektów w zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="32575-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="32575-137">Obecnie ten parametr nie działa nic.</span><span class="sxs-lookup"><span data-stu-id="32575-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="32575-138">— Pomiń</span><span class="sxs-lookup"><span data-stu-id="32575-138">-Skip</span></span>
<span data-ttu-id="32575-139">Ignoruje pierwsze obiekty N, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="32575-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="32575-140">— najpierw</span><span class="sxs-lookup"><span data-stu-id="32575-140">-First</span></span>
<span data-ttu-id="32575-141">Maksymalna liczba obiektów, które mają być zwracane.</span><span class="sxs-lookup"><span data-stu-id="32575-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="32575-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32575-142">CommonParameters</span></span>
<span data-ttu-id="32575-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32575-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32575-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32575-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32575-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32575-145">INPUTS</span></span>

### <span data-ttu-id="32575-146">System.String</span><span class="sxs-lookup"><span data-stu-id="32575-146">System.String</span></span>

## <span data-ttu-id="32575-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32575-147">OUTPUTS</span></span>

### <span data-ttu-id="32575-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="32575-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="32575-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="32575-149">NOTES</span></span>

## <span data-ttu-id="32575-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32575-150">RELATED LINKS</span></span>

[<span data-ttu-id="32575-151">New-AzadUser</span><span class="sxs-lookup"><span data-stu-id="32575-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="32575-152">Update-azadUser</span><span class="sxs-lookup"><span data-stu-id="32575-152">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="32575-153">Remove-AzadUser</span><span class="sxs-lookup"><span data-stu-id="32575-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

