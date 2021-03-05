---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 759977fb861f0ff2f1ede1fb28af50448b5ba5ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984186"
---
# <span data-ttu-id="e9091-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e9091-101">Get-AzADApplication</span></span>

## <span data-ttu-id="e9091-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9091-102">SYNOPSIS</span></span>
<span data-ttu-id="e9091-103">Lista istniejących aplikacji usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e9091-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="e9091-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e9091-104">SYNTAX</span></span>

### <span data-ttu-id="e9091-105">EmptyParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e9091-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e9091-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9091-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e9091-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9091-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e9091-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9091-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e9091-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9091-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e9091-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9091-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="e9091-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="e9091-111">DESCRIPTION</span></span>
<span data-ttu-id="e9091-112">Lista istniejących aplikacji usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e9091-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="e9091-113">Odnośnik aplikacji może być przez obiekt ObjectId, ApplicationId, IdentyfikatorUri lub DisplayName.</span><span class="sxs-lookup"><span data-stu-id="e9091-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="e9091-114">Jeśli nie podano parametru, pobiera on wszystkie aplikacje w ramach dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e9091-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="e9091-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e9091-115">EXAMPLES</span></span>

### <span data-ttu-id="e9091-116">Przykład 1. Lista wszystkich aplikacji</span><span class="sxs-lookup"><span data-stu-id="e9091-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="e9091-117">Wyświetla listę wszystkich aplikacji w ramach dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e9091-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="e9091-118">Przykład 2. Lista aplikacji używających stronicowania</span><span class="sxs-lookup"><span data-stu-id="e9091-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="e9091-119">Wyświetla listę pierwszych 100 aplikacji w ramach dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e9091-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="e9091-120">Przykład 3. Uzyskiwanie aplikacji za pomocą identyfikatora URI</span><span class="sxs-lookup"><span data-stu-id="e9091-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="e9091-121">Pobiera aplikację z identyfikatorem uri jako " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="e9091-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="e9091-122">Przykład 4. Uzyskiwanie aplikacji według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="e9091-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="e9091-123">Pobiera aplikację o identyfikatorze obiektu "39e64ec6-569b-4030-8e1c-c3c519a05d69".</span><span class="sxs-lookup"><span data-stu-id="e9091-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="e9091-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9091-124">PARAMETERS</span></span>

### <span data-ttu-id="e9091-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e9091-125">-ApplicationId</span></span>
<span data-ttu-id="e9091-126">Identyfikator aplikacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="e9091-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="e9091-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9091-127">-DefaultProfile</span></span>
<span data-ttu-id="e9091-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e9091-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9091-129">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="e9091-129">-DisplayName</span></span>
<span data-ttu-id="e9091-130">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e9091-130">The display name of the application.</span></span>

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

### <span data-ttu-id="e9091-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="e9091-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="e9091-132">Pobieraj wszystkie aplikacje, zaczynając od nazwy wyświetlanej.</span><span class="sxs-lookup"><span data-stu-id="e9091-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="e9091-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="e9091-133">-IdentifierUri</span></span>
<span data-ttu-id="e9091-134">Unikatowy identyfikator Uri aplikacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="e9091-134">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="e9091-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e9091-135">-ObjectId</span></span>
<span data-ttu-id="e9091-136">Identyfikator obiektu aplikacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="e9091-136">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="e9091-137">- IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="e9091-137">-IncludeTotalCount</span></span>
<span data-ttu-id="e9091-138">Raportuje liczbę obiektów w zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="e9091-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="e9091-139">Obecnie ten parametr nie działa nic.</span><span class="sxs-lookup"><span data-stu-id="e9091-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="e9091-140">— Pomiń</span><span class="sxs-lookup"><span data-stu-id="e9091-140">-Skip</span></span>
<span data-ttu-id="e9091-141">Ignoruje pierwsze obiekty N, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="e9091-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="e9091-142">— najpierw</span><span class="sxs-lookup"><span data-stu-id="e9091-142">-First</span></span>
<span data-ttu-id="e9091-143">Maksymalna liczba obiektów, które mają być zwracane.</span><span class="sxs-lookup"><span data-stu-id="e9091-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="e9091-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9091-144">CommonParameters</span></span>
<span data-ttu-id="e9091-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9091-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9091-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9091-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9091-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9091-147">INPUTS</span></span>

### <span data-ttu-id="e9091-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e9091-148">System.String</span></span>

### <span data-ttu-id="e9091-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e9091-149">System.Guid</span></span>

## <span data-ttu-id="e9091-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9091-150">OUTPUTS</span></span>

### <span data-ttu-id="e9091-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e9091-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="e9091-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e9091-152">NOTES</span></span>

## <span data-ttu-id="e9091-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9091-153">RELATED LINKS</span></span>

[<span data-ttu-id="e9091-154">Remove-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="e9091-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="e9091-155">New-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="e9091-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="e9091-156">Get-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="e9091-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="e9091-157">Remove-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="e9091-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="e9091-158">New-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="e9091-158">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="e9091-159">Update-azadApplication</span><span class="sxs-lookup"><span data-stu-id="e9091-159">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

