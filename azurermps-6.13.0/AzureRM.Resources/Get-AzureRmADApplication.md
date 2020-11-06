---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: d36bca60f722498beaa831c2a630b23d8a709019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544879"
---
# <span data-ttu-id="22dad-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="22dad-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="22dad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22dad-102">SYNOPSIS</span></span>
<span data-ttu-id="22dad-103">Wyświetla istniejące aplikacje usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="22dad-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22dad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22dad-104">SYNTAX</span></span>

### <span data-ttu-id="22dad-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="22dad-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="22dad-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22dad-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="22dad-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22dad-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="22dad-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="22dad-108">SearchStringParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="22dad-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="22dad-109">DisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="22dad-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="22dad-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="22dad-111">Opis</span><span class="sxs-lookup"><span data-stu-id="22dad-111">DESCRIPTION</span></span>
<span data-ttu-id="22dad-112">Wyświetla istniejące aplikacje usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="22dad-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="22dad-113">Wyszukiwanie aplikacji można przeprowadzić przez ObjectId, identyfikator aplikacji, IdentifierUri lub DisplayName.</span><span class="sxs-lookup"><span data-stu-id="22dad-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="22dad-114">Jeśli nie podano parametru, pobiera wszystkie aplikacje w ramach dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="22dad-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="22dad-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22dad-115">EXAMPLES</span></span>

### <span data-ttu-id="22dad-116">Przykład 1-Lista wszystkich aplikacji</span><span class="sxs-lookup"><span data-stu-id="22dad-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzureRmADApplication
```

<span data-ttu-id="22dad-117">Wyświetla listę wszystkich aplikacji w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="22dad-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="22dad-118">Przykład 2-Lista aplikacji przy użyciu stronicowania</span><span class="sxs-lookup"><span data-stu-id="22dad-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzureRmADApplication -First 100
```

<span data-ttu-id="22dad-119">Wyświetla listę pierwszych aplikacji 100 w ramach dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="22dad-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="22dad-120">Przykład 3 — Uzyskaj identyfikator aplikacji według identyfikatora URI</span><span class="sxs-lookup"><span data-stu-id="22dad-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="22dad-121">Pobiera aplikację o identyfikatorze URI " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="22dad-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="22dad-122">Przykład 4 — Pobierz aplikację według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="22dad-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="22dad-123">Pobiera aplikację o identyfikatorze obiektu "39e64ec6-569b-4030-8e1c-c3c519a05d69".</span><span class="sxs-lookup"><span data-stu-id="22dad-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="22dad-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22dad-124">PARAMETERS</span></span>

### <span data-ttu-id="22dad-125">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="22dad-125">-ApplicationId</span></span>
<span data-ttu-id="22dad-126">Identyfikator aplikacji, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="22dad-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="22dad-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22dad-127">-DefaultProfile</span></span>
<span data-ttu-id="22dad-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="22dad-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22dad-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="22dad-129">-DisplayName</span></span>
<span data-ttu-id="22dad-130">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="22dad-130">The display name of the application.</span></span>

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

### <span data-ttu-id="22dad-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="22dad-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="22dad-132">Pobierz wszystkie aplikacje, rozpoczynając od nazwy wyświetlanej.</span><span class="sxs-lookup"><span data-stu-id="22dad-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="22dad-133">-First</span><span class="sxs-lookup"><span data-stu-id="22dad-133">-First</span></span>
<span data-ttu-id="22dad-134">Maksymalna liczba obiektów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="22dad-134">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="22dad-135">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="22dad-135">-IdentifierUri</span></span>
<span data-ttu-id="22dad-136">Unikatowy identyfikator identyfikator URI aplikacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="22dad-136">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="22dad-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="22dad-137">-IncludeTotalCount</span></span>
<span data-ttu-id="22dad-138">Wyświetla liczbę obiektów w zbiorze danych.</span><span class="sxs-lookup"><span data-stu-id="22dad-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="22dad-139">Obecnie ten parametr nie wykonuje żadnych działań.</span><span class="sxs-lookup"><span data-stu-id="22dad-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="22dad-140">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="22dad-140">-ObjectId</span></span>
<span data-ttu-id="22dad-141">Identyfikator obiektu aplikacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="22dad-141">The object id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22dad-142">-Skip</span><span class="sxs-lookup"><span data-stu-id="22dad-142">-Skip</span></span>
<span data-ttu-id="22dad-143">Ignoruje pierwsze N obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="22dad-143">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="22dad-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22dad-144">CommonParameters</span></span>
<span data-ttu-id="22dad-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22dad-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22dad-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22dad-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22dad-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22dad-147">INPUTS</span></span>

### <span data-ttu-id="22dad-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="22dad-148">System.Guid</span></span>

### <span data-ttu-id="22dad-149">System. String</span><span class="sxs-lookup"><span data-stu-id="22dad-149">System.String</span></span>

## <span data-ttu-id="22dad-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22dad-150">OUTPUTS</span></span>

### <span data-ttu-id="22dad-151">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="22dad-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="22dad-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22dad-152">NOTES</span></span>

## <span data-ttu-id="22dad-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22dad-153">RELATED LINKS</span></span>

[<span data-ttu-id="22dad-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="22dad-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="22dad-155">Nowe — AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="22dad-155">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="22dad-156">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="22dad-156">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="22dad-157">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="22dad-157">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="22dad-158">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="22dad-158">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="22dad-159">Nowe — AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="22dad-159">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

