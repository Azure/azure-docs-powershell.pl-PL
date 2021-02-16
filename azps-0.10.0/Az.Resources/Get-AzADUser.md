---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: b5690dfc1d85483b10fc7cd08606c4555784e8e0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398737"
---
# <span data-ttu-id="cc050-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="cc050-101">Get-AzADUser</span></span>

## <span data-ttu-id="cc050-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc050-102">SYNOPSIS</span></span>
<span data-ttu-id="cc050-103">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cc050-103">Filters active directory users.</span></span>

## <span data-ttu-id="cc050-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cc050-104">SYNTAX</span></span>

### <span data-ttu-id="cc050-105">EmptyParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="cc050-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cc050-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc050-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cc050-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc050-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cc050-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc050-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cc050-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc050-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cc050-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc050-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="cc050-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="cc050-111">DESCRIPTION</span></span>
<span data-ttu-id="cc050-112">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cc050-112">Filters active directory users.</span></span>

## <span data-ttu-id="cc050-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cc050-113">EXAMPLES</span></span>

### <span data-ttu-id="cc050-114">Przykład 1. Lista wszystkich użytkowników</span><span class="sxs-lookup"><span data-stu-id="cc050-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="cc050-115">Wyświetla listę wszystkich użytkowników usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="cc050-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="cc050-116">Przykład 2. Lista wszystkich użytkowników używających stronicowania</span><span class="sxs-lookup"><span data-stu-id="cc050-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="cc050-117">Wyświetla listę pierwszych 100 użytkowników usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="cc050-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="cc050-118">Przykład 3. Uzyskiwanie użytkownika usługi AD według głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="cc050-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="cc050-119">Pobiera użytkownika usługi AD o głównej nazwie użytkownika: " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="cc050-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="cc050-120">Przykład 4. Lista według ciągu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="cc050-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="cc050-121">Wyświetla listę wszystkich użytkowników usługi AD, których nazwa wyświetlana zaczyna się od "Jan".</span><span class="sxs-lookup"><span data-stu-id="cc050-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="cc050-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc050-122">PARAMETERS</span></span>

### <span data-ttu-id="cc050-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc050-123">-DefaultProfile</span></span>
<span data-ttu-id="cc050-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cc050-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc050-125">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="cc050-125">-DisplayName</span></span>
<span data-ttu-id="cc050-126">Nazwa wyświetlana użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cc050-126">The display name of the user.</span></span>

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

### <span data-ttu-id="cc050-127">— najpierw</span><span class="sxs-lookup"><span data-stu-id="cc050-127">-First</span></span>
<span data-ttu-id="cc050-128">Maksymalna liczba obiektów, które mają być zwracane.</span><span class="sxs-lookup"><span data-stu-id="cc050-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="cc050-129">- IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="cc050-129">-IncludeTotalCount</span></span>
<span data-ttu-id="cc050-130">Raportuje liczbę obiektów w zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="cc050-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="cc050-131">Obecnie ten parametr nie działa nic.</span><span class="sxs-lookup"><span data-stu-id="cc050-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="cc050-132">— Poczta</span><span class="sxs-lookup"><span data-stu-id="cc050-132">-Mail</span></span>
<span data-ttu-id="cc050-133">Poczta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cc050-133">The user mail.</span></span>

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

### <span data-ttu-id="cc050-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cc050-134">-ObjectId</span></span>
<span data-ttu-id="cc050-135">Identyfikator obiektu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cc050-135">Object id of the user.</span></span>

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

### <span data-ttu-id="cc050-136">— Pomiń</span><span class="sxs-lookup"><span data-stu-id="cc050-136">-Skip</span></span>
<span data-ttu-id="cc050-137">Ignoruje pierwsze obiekty N, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="cc050-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="cc050-138">—StartsWith</span><span class="sxs-lookup"><span data-stu-id="cc050-138">-StartsWith</span></span>
<span data-ttu-id="cc050-139">Umożliwia znalezienie użytkowników, którzy zaczynają się od podanego ciągu.</span><span class="sxs-lookup"><span data-stu-id="cc050-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="cc050-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cc050-140">-UserPrincipalName</span></span>
<span data-ttu-id="cc050-141">UpN użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cc050-141">UPN of the user.</span></span>

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

### <span data-ttu-id="cc050-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc050-142">CommonParameters</span></span>
<span data-ttu-id="cc050-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc050-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc050-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc050-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc050-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc050-145">INPUTS</span></span>

### <span data-ttu-id="cc050-146">System.String</span><span class="sxs-lookup"><span data-stu-id="cc050-146">System.String</span></span>

### <span data-ttu-id="cc050-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="cc050-147">System.Guid</span></span>

## <span data-ttu-id="cc050-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc050-148">OUTPUTS</span></span>

### <span data-ttu-id="cc050-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="cc050-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="cc050-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cc050-150">NOTES</span></span>

## <span data-ttu-id="cc050-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc050-151">RELATED LINKS</span></span>

[<span data-ttu-id="cc050-152">New-AzadUser</span><span class="sxs-lookup"><span data-stu-id="cc050-152">New-AzADUser</span></span>](./New-AzADUser.md)


[<span data-ttu-id="cc050-153">Remove-AzadUser</span><span class="sxs-lookup"><span data-stu-id="cc050-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

