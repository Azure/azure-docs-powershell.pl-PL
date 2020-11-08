---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 68344fcafa16187651615c95ec2fb41d0bbbfb82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221138"
---
# <span data-ttu-id="c4a59-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c4a59-101">Get-AzADApplication</span></span>

## <span data-ttu-id="c4a59-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4a59-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a59-103">Wyświetla istniejące aplikacje usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c4a59-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="c4a59-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4a59-104">SYNTAX</span></span>

### <span data-ttu-id="c4a59-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c4a59-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c4a59-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4a59-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c4a59-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4a59-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c4a59-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4a59-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c4a59-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4a59-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c4a59-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4a59-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="c4a59-111">Opis</span><span class="sxs-lookup"><span data-stu-id="c4a59-111">DESCRIPTION</span></span>
<span data-ttu-id="c4a59-112">Wyświetla istniejące aplikacje usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c4a59-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="c4a59-113">Wyszukiwanie aplikacji można przeprowadzić przez ObjectId, identyfikator aplikacji, IdentifierUri lub DisplayName.</span><span class="sxs-lookup"><span data-stu-id="c4a59-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="c4a59-114">Jeśli nie podano parametru, pobiera wszystkie aplikacje w ramach dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="c4a59-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="c4a59-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4a59-115">EXAMPLES</span></span>

### <span data-ttu-id="c4a59-116">Przykład 1-Lista wszystkich aplikacji</span><span class="sxs-lookup"><span data-stu-id="c4a59-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="c4a59-117">Wyświetla listę wszystkich aplikacji w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="c4a59-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="c4a59-118">Przykład 2-Lista aplikacji przy użyciu stronicowania</span><span class="sxs-lookup"><span data-stu-id="c4a59-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="c4a59-119">Wyświetla listę pierwszych aplikacji 100 w ramach dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="c4a59-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="c4a59-120">Przykład 3 — Uzyskaj identyfikator aplikacji według identyfikatora URI</span><span class="sxs-lookup"><span data-stu-id="c4a59-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="c4a59-121">Pobiera aplikację o identyfikatorze URI " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="c4a59-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="c4a59-122">Przykład 4 — Pobierz aplikację według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="c4a59-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="c4a59-123">Pobiera aplikację o identyfikatorze obiektu "39e64ec6-569b-4030-8e1c-c3c519a05d69".</span><span class="sxs-lookup"><span data-stu-id="c4a59-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="c4a59-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4a59-124">PARAMETERS</span></span>

### <span data-ttu-id="c4a59-125">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="c4a59-125">-ApplicationId</span></span>
<span data-ttu-id="c4a59-126">Identyfikator aplikacji, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="c4a59-126">The application id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a59-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a59-127">-DefaultProfile</span></span>
<span data-ttu-id="c4a59-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c4a59-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4a59-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c4a59-129">-DisplayName</span></span>
<span data-ttu-id="c4a59-130">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c4a59-130">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a59-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="c4a59-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="c4a59-132">Pobierz wszystkie aplikacje, rozpoczynając od nazwy wyświetlanej.</span><span class="sxs-lookup"><span data-stu-id="c4a59-132">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a59-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="c4a59-133">-IdentifierUri</span></span>
<span data-ttu-id="c4a59-134">Unikatowy identyfikator identyfikator URI aplikacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="c4a59-134">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a59-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c4a59-135">-ObjectId</span></span>
<span data-ttu-id="c4a59-136">Identyfikator obiektu aplikacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="c4a59-136">The object id of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a59-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="c4a59-137">-IncludeTotalCount</span></span>
<span data-ttu-id="c4a59-138">Wyświetla liczbę obiektów w zbiorze danych.</span><span class="sxs-lookup"><span data-stu-id="c4a59-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="c4a59-139">Obecnie ten parametr nie wykonuje żadnych działań.</span><span class="sxs-lookup"><span data-stu-id="c4a59-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="c4a59-140">-Skip</span><span class="sxs-lookup"><span data-stu-id="c4a59-140">-Skip</span></span>
<span data-ttu-id="c4a59-141">Ignoruje pierwsze N obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="c4a59-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="c4a59-142">-First</span><span class="sxs-lookup"><span data-stu-id="c4a59-142">-First</span></span>
<span data-ttu-id="c4a59-143">Maksymalna liczba obiektów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="c4a59-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="c4a59-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a59-144">CommonParameters</span></span>
<span data-ttu-id="c4a59-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a59-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a59-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4a59-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a59-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4a59-147">INPUTS</span></span>

### <span data-ttu-id="c4a59-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c4a59-148">System.String</span></span>

### <span data-ttu-id="c4a59-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c4a59-149">System.Guid</span></span>

## <span data-ttu-id="c4a59-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4a59-150">OUTPUTS</span></span>

### <span data-ttu-id="c4a59-151">Microsoft. Azure. Commands. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c4a59-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="c4a59-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4a59-152">NOTES</span></span>

## <span data-ttu-id="c4a59-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4a59-153">RELATED LINKS</span></span>

[<span data-ttu-id="c4a59-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c4a59-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="c4a59-155">Nowe — AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c4a59-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="c4a59-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c4a59-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="c4a59-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c4a59-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="c4a59-158">Nowe — AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c4a59-158">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="c4a59-159">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c4a59-159">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

