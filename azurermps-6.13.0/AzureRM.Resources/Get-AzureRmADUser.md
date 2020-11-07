---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: b19571025aeb6349277e9ae366146774862e8a80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717055"
---
# <span data-ttu-id="709f2-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="709f2-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="709f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="709f2-102">SYNOPSIS</span></span>
<span data-ttu-id="709f2-103">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="709f2-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="709f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="709f2-104">SYNTAX</span></span>

### <span data-ttu-id="709f2-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="709f2-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="709f2-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="709f2-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="709f2-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="709f2-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="709f2-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="709f2-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="709f2-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="709f2-109">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="709f2-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="709f2-110">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="709f2-111">Opis</span><span class="sxs-lookup"><span data-stu-id="709f2-111">DESCRIPTION</span></span>
<span data-ttu-id="709f2-112">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="709f2-112">Filters active directory users.</span></span>

## <span data-ttu-id="709f2-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="709f2-113">EXAMPLES</span></span>

### <span data-ttu-id="709f2-114">Przykład 1-Lista wszystkich użytkowników</span><span class="sxs-lookup"><span data-stu-id="709f2-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="709f2-115">Wyświetla listę wszystkich użytkowników usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="709f2-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="709f2-116">Przykład 2 — Lista wszystkich użytkowników korzystających z stronicowania</span><span class="sxs-lookup"><span data-stu-id="709f2-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzureRmADUser -First 100
```

<span data-ttu-id="709f2-117">Wyświetla listę pierwszych 100 użytkowników usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="709f2-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="709f2-118">Przykład 3 — Uzyskaj użytkownika usługi AD według głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="709f2-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="709f2-119">Pobiera użytkownika usługi AD przy użyciu głównej nazwy użytkownika " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="709f2-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="709f2-120">Przykład 4-listowy według ciągu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="709f2-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="709f2-121">Wyświetla listę wszystkich użytkowników usługi AD, których nazwa wyświetlana rozpoczyna się od "Janusz".</span><span class="sxs-lookup"><span data-stu-id="709f2-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="709f2-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="709f2-122">PARAMETERS</span></span>

### <span data-ttu-id="709f2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="709f2-123">-DefaultProfile</span></span>
<span data-ttu-id="709f2-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="709f2-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="709f2-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="709f2-125">-DisplayName</span></span>
<span data-ttu-id="709f2-126">Nazwa wyświetlana użytkownika.</span><span class="sxs-lookup"><span data-stu-id="709f2-126">The display name of the user.</span></span>

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

### <span data-ttu-id="709f2-127">-First</span><span class="sxs-lookup"><span data-stu-id="709f2-127">-First</span></span>
<span data-ttu-id="709f2-128">Maksymalna liczba obiektów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="709f2-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="709f2-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="709f2-129">-IncludeTotalCount</span></span>
<span data-ttu-id="709f2-130">Wyświetla liczbę obiektów w zbiorze danych.</span><span class="sxs-lookup"><span data-stu-id="709f2-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="709f2-131">Obecnie ten parametr nie wykonuje żadnych działań.</span><span class="sxs-lookup"><span data-stu-id="709f2-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="709f2-132">-Mail</span><span class="sxs-lookup"><span data-stu-id="709f2-132">-Mail</span></span>
<span data-ttu-id="709f2-133">Poczta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="709f2-133">The user mail.</span></span>

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

### <span data-ttu-id="709f2-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="709f2-134">-ObjectId</span></span>
<span data-ttu-id="709f2-135">Identyfikator obiektu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="709f2-135">Object id of the user.</span></span>

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

### <span data-ttu-id="709f2-136">-Skip</span><span class="sxs-lookup"><span data-stu-id="709f2-136">-Skip</span></span>
<span data-ttu-id="709f2-137">Ignoruje pierwsze N obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="709f2-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="709f2-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="709f2-138">-StartsWith</span></span>
<span data-ttu-id="709f2-139">Służy do znajdowania użytkowników zaczynających się od podanego ciągu.</span><span class="sxs-lookup"><span data-stu-id="709f2-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="709f2-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="709f2-140">-UserPrincipalName</span></span>
<span data-ttu-id="709f2-141">UPN użytkownika.</span><span class="sxs-lookup"><span data-stu-id="709f2-141">UPN of the user.</span></span>

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

### <span data-ttu-id="709f2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="709f2-142">CommonParameters</span></span>
<span data-ttu-id="709f2-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="709f2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="709f2-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="709f2-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="709f2-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="709f2-145">INPUTS</span></span>

### <span data-ttu-id="709f2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="709f2-146">System.String</span></span>

### <span data-ttu-id="709f2-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="709f2-147">System.Guid</span></span>

## <span data-ttu-id="709f2-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="709f2-148">OUTPUTS</span></span>

### <span data-ttu-id="709f2-149">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="709f2-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="709f2-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="709f2-150">NOTES</span></span>

## <span data-ttu-id="709f2-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="709f2-151">RELATED LINKS</span></span>

[<span data-ttu-id="709f2-152">Nowe — AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="709f2-152">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="709f2-153">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="709f2-153">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="709f2-154">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="709f2-154">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

