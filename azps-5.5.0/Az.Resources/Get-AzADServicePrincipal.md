---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: b467d629b578e9f9883dac4c0a8e268f9007a373
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178898"
---
# <span data-ttu-id="c1cff-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c1cff-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="c1cff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1cff-102">SYNOPSIS</span></span>
<span data-ttu-id="c1cff-103">Filtruje podmioty zabezpieczeń usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c1cff-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="c1cff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c1cff-104">SYNTAX</span></span>

### <span data-ttu-id="c1cff-105">EmptyParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c1cff-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c1cff-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1cff-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c1cff-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1cff-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c1cff-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1cff-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c1cff-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1cff-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c1cff-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1cff-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c1cff-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1cff-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="c1cff-112">OPIS</span><span class="sxs-lookup"><span data-stu-id="c1cff-112">DESCRIPTION</span></span>
<span data-ttu-id="c1cff-113">Filtruje podmioty zabezpieczeń usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c1cff-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="c1cff-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c1cff-114">EXAMPLES</span></span>

### <span data-ttu-id="c1cff-115">Przykład 1. Lista głównych podmiotów usługi AD</span><span class="sxs-lookup"><span data-stu-id="c1cff-115">Example 1: List AD service principals</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="c1cff-116">Wyświetla listę wszystkich głównych podmiotów usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="c1cff-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="c1cff-117">Przykład 2. Lista głównych podmiotów usługi AD przy użyciu stronicowania</span><span class="sxs-lookup"><span data-stu-id="c1cff-117">Example 2: List AD service principals using paging</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="c1cff-118">Wyświetla listę pierwszych 100 głównych podmiotów usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="c1cff-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="c1cff-119">Przykład 3. Lista głównych podmiotów usługi według sieci SPN</span><span class="sxs-lookup"><span data-stu-id="c1cff-119">Example 3: List service principals by SPN</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="c1cff-120">Wyświetla listę głównych podmiotów usługi ze spN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span><span class="sxs-lookup"><span data-stu-id="c1cff-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="c1cff-121">Przykład 4. Lista podmiotów zabezpieczeń usługi według ciągu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="c1cff-121">Example 4: List service principals by search string</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="c1cff-122">Wyświetla listę wszystkich głównych podmiotów usługi AD, których nazwa wyświetlana zaczyna się od "sieci Web".</span><span class="sxs-lookup"><span data-stu-id="c1cff-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="c1cff-123">Przykład 5. Lista głównych podmiotów usług za pomocą rur</span><span class="sxs-lookup"><span data-stu-id="c1cff-123">Example 5: List service principals by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="c1cff-124">Pobiera aplikację AD z identyfikatorem obiektu "39e64ec6-569b-4030-8e1c-c3c519a05d69" i potokuje ją do polecenia cmdlet programu Get-AzADServicePrincipal, aby wyświetlić listę wszystkich głównych podmiotów usługi dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c1cff-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="c1cff-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1cff-125">PARAMETERS</span></span>

### <span data-ttu-id="c1cff-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c1cff-126">-ApplicationId</span></span>
<span data-ttu-id="c1cff-127">Identyfikator aplikacji podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="c1cff-127">The service principal application id.</span></span>

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

### <span data-ttu-id="c1cff-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="c1cff-128">-ApplicationObject</span></span>
<span data-ttu-id="c1cff-129">Obiekt aplikacji, którego podmiot zabezpieczeń usługi jest pobierany.</span><span class="sxs-lookup"><span data-stu-id="c1cff-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cff-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1cff-130">-DefaultProfile</span></span>
<span data-ttu-id="c1cff-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c1cff-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1cff-132">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="c1cff-132">-DisplayName</span></span>
<span data-ttu-id="c1cff-133">Nazwa wyświetlana podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="c1cff-133">The service principal display name.</span></span>

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

### <span data-ttu-id="c1cff-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="c1cff-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="c1cff-135">Ciąg wyszukiwania podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="c1cff-135">The service principal search string.</span></span>

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

### <span data-ttu-id="c1cff-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c1cff-136">-ObjectId</span></span>
<span data-ttu-id="c1cff-137">Identyfikator obiektu podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="c1cff-137">Object id of the service principal.</span></span>

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

### <span data-ttu-id="c1cff-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c1cff-138">-ServicePrincipalName</span></span>
<span data-ttu-id="c1cff-139">SpN usługi.</span><span class="sxs-lookup"><span data-stu-id="c1cff-139">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cff-140">- IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="c1cff-140">-IncludeTotalCount</span></span>
<span data-ttu-id="c1cff-141">Raportuje liczbę obiektów w zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="c1cff-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="c1cff-142">Obecnie ten parametr nie działa nic.</span><span class="sxs-lookup"><span data-stu-id="c1cff-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="c1cff-143">— Pomiń</span><span class="sxs-lookup"><span data-stu-id="c1cff-143">-Skip</span></span>
<span data-ttu-id="c1cff-144">Ignoruje pierwsze obiekty N, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="c1cff-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="c1cff-145">— Najpierw</span><span class="sxs-lookup"><span data-stu-id="c1cff-145">-First</span></span>
<span data-ttu-id="c1cff-146">Maksymalna liczba obiektów, które mają być zwracane.</span><span class="sxs-lookup"><span data-stu-id="c1cff-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="c1cff-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1cff-147">CommonParameters</span></span>
<span data-ttu-id="c1cff-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1cff-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1cff-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1cff-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1cff-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1cff-150">INPUTS</span></span>

### <span data-ttu-id="c1cff-151">System.String</span><span class="sxs-lookup"><span data-stu-id="c1cff-151">System.String</span></span>

### <span data-ttu-id="c1cff-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c1cff-152">System.Guid</span></span>

### <span data-ttu-id="c1cff-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c1cff-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="c1cff-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1cff-154">OUTPUTS</span></span>

### <span data-ttu-id="c1cff-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c1cff-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="c1cff-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c1cff-156">NOTES</span></span>

## <span data-ttu-id="c1cff-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1cff-157">RELATED LINKS</span></span>

[<span data-ttu-id="c1cff-158">New-AzadServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c1cff-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="c1cff-159">Update-AzadServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c1cff-159">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="c1cff-160">Remove-AzadServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c1cff-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="c1cff-161">Get-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="c1cff-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="c1cff-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c1cff-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

