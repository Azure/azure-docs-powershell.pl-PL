---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: d0391b47e4060b2b93206c8e4d2722ca682a0db4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895945"
---
# <span data-ttu-id="74d91-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="74d91-101">Get-AzADUser</span></span>

## <span data-ttu-id="74d91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74d91-102">SYNOPSIS</span></span>
<span data-ttu-id="74d91-103">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="74d91-103">Filters active directory users.</span></span>

## <span data-ttu-id="74d91-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74d91-104">SYNTAX</span></span>

### <span data-ttu-id="74d91-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="74d91-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="74d91-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="74d91-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="74d91-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="74d91-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="74d91-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74d91-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="74d91-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="74d91-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="74d91-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="74d91-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="74d91-111">Opis</span><span class="sxs-lookup"><span data-stu-id="74d91-111">DESCRIPTION</span></span>
<span data-ttu-id="74d91-112">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="74d91-112">Filters active directory users.</span></span>

## <span data-ttu-id="74d91-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74d91-113">EXAMPLES</span></span>

### <span data-ttu-id="74d91-114">Przykład 1-Lista wszystkich użytkowników</span><span class="sxs-lookup"><span data-stu-id="74d91-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="74d91-115">Wyświetla listę wszystkich użytkowników usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="74d91-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="74d91-116">Przykład 2 — Lista wszystkich użytkowników korzystających z stronicowania</span><span class="sxs-lookup"><span data-stu-id="74d91-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="74d91-117">Wyświetla listę pierwszych 100 użytkowników usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="74d91-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="74d91-118">Przykład 3 — Uzyskaj użytkownika usługi AD według głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="74d91-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="74d91-119">Pobiera użytkownika usługi AD przy użyciu głównej nazwy użytkownika " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="74d91-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="74d91-120">Przykład 4-listowy według ciągu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="74d91-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="74d91-121">Wyświetla listę wszystkich użytkowników usługi AD, których nazwa wyświetlana rozpoczyna się od "Janusz".</span><span class="sxs-lookup"><span data-stu-id="74d91-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="74d91-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74d91-122">PARAMETERS</span></span>

### <span data-ttu-id="74d91-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d91-123">-DefaultProfile</span></span>
<span data-ttu-id="74d91-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="74d91-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74d91-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="74d91-125">-DisplayName</span></span>
<span data-ttu-id="74d91-126">Nazwa wyświetlana użytkownika.</span><span class="sxs-lookup"><span data-stu-id="74d91-126">The display name of the user.</span></span>

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

### <span data-ttu-id="74d91-127">-Mail</span><span class="sxs-lookup"><span data-stu-id="74d91-127">-Mail</span></span>
<span data-ttu-id="74d91-128">Poczta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="74d91-128">The user mail.</span></span>

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

### <span data-ttu-id="74d91-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="74d91-129">-ObjectId</span></span>
<span data-ttu-id="74d91-130">Identyfikator obiektu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="74d91-130">Object id of the user.</span></span>

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

### <span data-ttu-id="74d91-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="74d91-131">-StartsWith</span></span>
<span data-ttu-id="74d91-132">Służy do znajdowania użytkowników zaczynających się od podanego ciągu.</span><span class="sxs-lookup"><span data-stu-id="74d91-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="74d91-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="74d91-133">-UserPrincipalName</span></span>
<span data-ttu-id="74d91-134">UPN użytkownika.</span><span class="sxs-lookup"><span data-stu-id="74d91-134">UPN of the user.</span></span>

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

### <span data-ttu-id="74d91-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="74d91-135">-IncludeTotalCount</span></span>
<span data-ttu-id="74d91-136">Wyświetla liczbę obiektów w zbiorze danych.</span><span class="sxs-lookup"><span data-stu-id="74d91-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="74d91-137">Obecnie ten parametr nie wykonuje żadnych działań.</span><span class="sxs-lookup"><span data-stu-id="74d91-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="74d91-138">-Skip</span><span class="sxs-lookup"><span data-stu-id="74d91-138">-Skip</span></span>
<span data-ttu-id="74d91-139">Ignoruje pierwsze N obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="74d91-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="74d91-140">-First</span><span class="sxs-lookup"><span data-stu-id="74d91-140">-First</span></span>
<span data-ttu-id="74d91-141">Maksymalna liczba obiektów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="74d91-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="74d91-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d91-142">CommonParameters</span></span>
<span data-ttu-id="74d91-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74d91-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d91-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74d91-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d91-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74d91-145">INPUTS</span></span>

### <span data-ttu-id="74d91-146">System. String</span><span class="sxs-lookup"><span data-stu-id="74d91-146">System.String</span></span>

## <span data-ttu-id="74d91-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74d91-147">OUTPUTS</span></span>

### <span data-ttu-id="74d91-148">Microsoft. Azure. Commands. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="74d91-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="74d91-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74d91-149">NOTES</span></span>

## <span data-ttu-id="74d91-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74d91-150">RELATED LINKS</span></span>

[<span data-ttu-id="74d91-151">Nowe — AzADUser</span><span class="sxs-lookup"><span data-stu-id="74d91-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="74d91-152">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="74d91-152">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="74d91-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="74d91-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

