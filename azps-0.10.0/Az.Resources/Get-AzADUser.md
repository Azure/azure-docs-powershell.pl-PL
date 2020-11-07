---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 34a00ed29d40d8824ac0f2d24f5275bb7c0a0164
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892622"
---
# <span data-ttu-id="f8887-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="f8887-101">Get-AzADUser</span></span>

## <span data-ttu-id="f8887-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8887-102">SYNOPSIS</span></span>
<span data-ttu-id="f8887-103">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f8887-103">Filters active directory users.</span></span>

## <span data-ttu-id="f8887-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8887-104">SYNTAX</span></span>

### <span data-ttu-id="f8887-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f8887-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f8887-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8887-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f8887-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8887-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f8887-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8887-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f8887-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8887-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f8887-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8887-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="f8887-111">Opis</span><span class="sxs-lookup"><span data-stu-id="f8887-111">DESCRIPTION</span></span>
<span data-ttu-id="f8887-112">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f8887-112">Filters active directory users.</span></span>

## <span data-ttu-id="f8887-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8887-113">EXAMPLES</span></span>

### <span data-ttu-id="f8887-114">Przykład 1-Lista wszystkich użytkowników</span><span class="sxs-lookup"><span data-stu-id="f8887-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="f8887-115">Wyświetla listę wszystkich użytkowników usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="f8887-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="f8887-116">Przykład 2 — Lista wszystkich użytkowników korzystających z stronicowania</span><span class="sxs-lookup"><span data-stu-id="f8887-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="f8887-117">Wyświetla listę pierwszych 100 użytkowników usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="f8887-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="f8887-118">Przykład 3 — Uzyskaj użytkownika usługi AD według głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="f8887-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="f8887-119">Pobiera użytkownika usługi AD przy użyciu głównej nazwy użytkownika " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="f8887-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="f8887-120">Przykład 4-listowy według ciągu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="f8887-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="f8887-121">Wyświetla listę wszystkich użytkowników usługi AD, których nazwa wyświetlana rozpoczyna się od "Janusz".</span><span class="sxs-lookup"><span data-stu-id="f8887-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="f8887-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8887-122">PARAMETERS</span></span>

### <span data-ttu-id="f8887-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8887-123">-DefaultProfile</span></span>
<span data-ttu-id="f8887-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f8887-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8887-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f8887-125">-DisplayName</span></span>
<span data-ttu-id="f8887-126">Nazwa wyświetlana użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f8887-126">The display name of the user.</span></span>

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

### <span data-ttu-id="f8887-127">-First</span><span class="sxs-lookup"><span data-stu-id="f8887-127">-First</span></span>
<span data-ttu-id="f8887-128">Maksymalna liczba obiektów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="f8887-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="f8887-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="f8887-129">-IncludeTotalCount</span></span>
<span data-ttu-id="f8887-130">Wyświetla liczbę obiektów w zbiorze danych.</span><span class="sxs-lookup"><span data-stu-id="f8887-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="f8887-131">Obecnie ten parametr nie wykonuje żadnych działań.</span><span class="sxs-lookup"><span data-stu-id="f8887-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="f8887-132">-Mail</span><span class="sxs-lookup"><span data-stu-id="f8887-132">-Mail</span></span>
<span data-ttu-id="f8887-133">Poczta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f8887-133">The user mail.</span></span>

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

### <span data-ttu-id="f8887-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f8887-134">-ObjectId</span></span>
<span data-ttu-id="f8887-135">Identyfikator obiektu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f8887-135">Object id of the user.</span></span>

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

### <span data-ttu-id="f8887-136">-Skip</span><span class="sxs-lookup"><span data-stu-id="f8887-136">-Skip</span></span>
<span data-ttu-id="f8887-137">Ignoruje pierwsze N obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="f8887-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="f8887-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="f8887-138">-StartsWith</span></span>
<span data-ttu-id="f8887-139">Służy do znajdowania użytkowników zaczynających się od podanego ciągu.</span><span class="sxs-lookup"><span data-stu-id="f8887-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="f8887-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f8887-140">-UserPrincipalName</span></span>
<span data-ttu-id="f8887-141">UPN użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f8887-141">UPN of the user.</span></span>

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

### <span data-ttu-id="f8887-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8887-142">CommonParameters</span></span>
<span data-ttu-id="f8887-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8887-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8887-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8887-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8887-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8887-145">INPUTS</span></span>

### <span data-ttu-id="f8887-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f8887-146">System.String</span></span>

### <span data-ttu-id="f8887-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f8887-147">System.Guid</span></span>

## <span data-ttu-id="f8887-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8887-148">OUTPUTS</span></span>

### <span data-ttu-id="f8887-149">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="f8887-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="f8887-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8887-150">NOTES</span></span>

## <span data-ttu-id="f8887-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8887-151">RELATED LINKS</span></span>

[<span data-ttu-id="f8887-152">Nowe — AzADUser</span><span class="sxs-lookup"><span data-stu-id="f8887-152">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="f8887-153">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="f8887-153">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="f8887-154">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="f8887-154">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

