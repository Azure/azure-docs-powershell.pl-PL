---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 80df38532d5d5ce14b27f40bed04678e80752fca
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406999"
---
# <span data-ttu-id="1561f-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="1561f-101">Get-AzADUser</span></span>

## <span data-ttu-id="1561f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1561f-102">SYNOPSIS</span></span>
<span data-ttu-id="1561f-103">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1561f-103">Filters active directory users.</span></span>

## <span data-ttu-id="1561f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1561f-104">SYNTAX</span></span>

### <span data-ttu-id="1561f-105">EmptyParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="1561f-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1561f-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1561f-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1561f-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1561f-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1561f-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1561f-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1561f-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="1561f-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1561f-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="1561f-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="1561f-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="1561f-111">DESCRIPTION</span></span>
<span data-ttu-id="1561f-112">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1561f-112">Filters active directory users.</span></span>

## <span data-ttu-id="1561f-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1561f-113">EXAMPLES</span></span>

### <span data-ttu-id="1561f-114">Przykład 1. Lista wszystkich użytkowników</span><span class="sxs-lookup"><span data-stu-id="1561f-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="1561f-115">Wyświetla listę wszystkich użytkowników usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="1561f-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="1561f-116">Przykład 2. Lista wszystkich użytkowników używających stronicowania</span><span class="sxs-lookup"><span data-stu-id="1561f-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="1561f-117">Wyświetla listę pierwszych 100 użytkowników usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="1561f-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="1561f-118">Przykład 3. Uzyskiwanie użytkownika usługi AD według głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="1561f-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="1561f-119">Pobiera użytkownika usługi AD o głównej nazwie użytkownika" foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="1561f-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="1561f-120">Przykład 4. Lista według ciągu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="1561f-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="1561f-121">Wyświetla listę wszystkich użytkowników usługi AD, których nazwa wyświetlana zaczyna się od "Jan".</span><span class="sxs-lookup"><span data-stu-id="1561f-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="1561f-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1561f-122">PARAMETERS</span></span>

### <span data-ttu-id="1561f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1561f-123">-DefaultProfile</span></span>
<span data-ttu-id="1561f-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1561f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1561f-125">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="1561f-125">-DisplayName</span></span>
<span data-ttu-id="1561f-126">Nazwa wyświetlana użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1561f-126">The display name of the user.</span></span>

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

### <span data-ttu-id="1561f-127">— Poczta</span><span class="sxs-lookup"><span data-stu-id="1561f-127">-Mail</span></span>
<span data-ttu-id="1561f-128">Poczta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1561f-128">The user mail.</span></span>

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

### <span data-ttu-id="1561f-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1561f-129">-ObjectId</span></span>
<span data-ttu-id="1561f-130">Identyfikator obiektu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1561f-130">Object id of the user.</span></span>

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

### <span data-ttu-id="1561f-131">—StartsWith</span><span class="sxs-lookup"><span data-stu-id="1561f-131">-StartsWith</span></span>
<span data-ttu-id="1561f-132">Umożliwia znalezienie użytkowników, którzy zaczynają się od podanego ciągu.</span><span class="sxs-lookup"><span data-stu-id="1561f-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="1561f-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="1561f-133">-UserPrincipalName</span></span>
<span data-ttu-id="1561f-134">UpN użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1561f-134">UPN of the user.</span></span>

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

### <span data-ttu-id="1561f-135">- IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="1561f-135">-IncludeTotalCount</span></span>
<span data-ttu-id="1561f-136">Raportuje liczbę obiektów w zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="1561f-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="1561f-137">Obecnie ten parametr nie działa nic.</span><span class="sxs-lookup"><span data-stu-id="1561f-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="1561f-138">— Pomiń</span><span class="sxs-lookup"><span data-stu-id="1561f-138">-Skip</span></span>
<span data-ttu-id="1561f-139">Ignoruje pierwsze obiekty N, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="1561f-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="1561f-140">— Najpierw</span><span class="sxs-lookup"><span data-stu-id="1561f-140">-First</span></span>
<span data-ttu-id="1561f-141">Maksymalna liczba obiektów, które mają być zwracane.</span><span class="sxs-lookup"><span data-stu-id="1561f-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="1561f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1561f-142">CommonParameters</span></span>
<span data-ttu-id="1561f-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1561f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1561f-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1561f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1561f-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1561f-145">INPUTS</span></span>

### <span data-ttu-id="1561f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="1561f-146">System.String</span></span>

## <span data-ttu-id="1561f-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1561f-147">OUTPUTS</span></span>

### <span data-ttu-id="1561f-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="1561f-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="1561f-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1561f-149">NOTES</span></span>

## <span data-ttu-id="1561f-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1561f-150">RELATED LINKS</span></span>

[<span data-ttu-id="1561f-151">New-AzadUser</span><span class="sxs-lookup"><span data-stu-id="1561f-151">New-AzADUser</span></span>](./New-AzADUser.md)


[<span data-ttu-id="1561f-152">Remove-AzadUser</span><span class="sxs-lookup"><span data-stu-id="1561f-152">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

