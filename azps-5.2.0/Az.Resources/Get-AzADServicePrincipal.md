---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: b467d629b578e9f9883dac4c0a8e268f9007a373
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355642"
---
# <span data-ttu-id="dd46a-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dd46a-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="dd46a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd46a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd46a-103">Umożliwia filtrowanie podmiotów zabezpieczeń usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dd46a-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="dd46a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd46a-104">SYNTAX</span></span>

### <span data-ttu-id="dd46a-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dd46a-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="dd46a-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd46a-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="dd46a-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd46a-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="dd46a-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd46a-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="dd46a-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd46a-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="dd46a-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd46a-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="dd46a-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd46a-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="dd46a-112">Opis</span><span class="sxs-lookup"><span data-stu-id="dd46a-112">DESCRIPTION</span></span>
<span data-ttu-id="dd46a-113">Umożliwia filtrowanie podmiotów zabezpieczeń usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dd46a-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="dd46a-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd46a-114">EXAMPLES</span></span>

### <span data-ttu-id="dd46a-115">Przykład 1: Lista podmiotów usługi AD</span><span class="sxs-lookup"><span data-stu-id="dd46a-115">Example 1: List AD service principals</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="dd46a-116">Wyświetla listę wszystkich podmiotów zabezpieczeń usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="dd46a-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="dd46a-117">Przykład 2: wyświetlanie podmiotów zabezpieczeń usługi AD przy użyciu stronicowania</span><span class="sxs-lookup"><span data-stu-id="dd46a-117">Example 2: List AD service principals using paging</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="dd46a-118">Wyświetla listę pierwszych 100 głównych usług REKLAMowych w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="dd46a-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="dd46a-119">Przykład 3: Wyświetlanie listy podmiotów usługi według nazwy SPN</span><span class="sxs-lookup"><span data-stu-id="dd46a-119">Example 3: List service principals by SPN</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="dd46a-120">Wyświetla listę podmiotów usługi za pomocą nazwy SPN "36f81fc3-b00f-48cd-8218-3879f51ff39f".</span><span class="sxs-lookup"><span data-stu-id="dd46a-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="dd46a-121">Przykład 4: Wyświetlanie listy podmiotów usługi według ciągu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="dd46a-121">Example 4: List service principals by search string</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="dd46a-122">Wyświetla listę wszystkich podmiotów nazw usługi AD, których nazwa wyświetlana rozpoczyna się od "Web".</span><span class="sxs-lookup"><span data-stu-id="dd46a-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="dd46a-123">Przykład 5: Wyświetlanie listy podmiotów usługi według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="dd46a-123">Example 5: List service principals by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="dd46a-124">Pobiera aplikację reklamy o identyfikatorze obiektu "39e64ec6-569b-4030-8e1c-c3c519a05d69" i przekazuje ją do polecenia cmdlet Get-AzADServicePrincipal, aby wyświetlić listę wszystkich głównych usług dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dd46a-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="dd46a-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd46a-125">PARAMETERS</span></span>

### <span data-ttu-id="dd46a-126">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="dd46a-126">-ApplicationId</span></span>
<span data-ttu-id="dd46a-127">Identyfikator głównej aplikacji usługi.</span><span class="sxs-lookup"><span data-stu-id="dd46a-127">The service principal application id.</span></span>

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

### <span data-ttu-id="dd46a-128">-Applicationobject</span><span class="sxs-lookup"><span data-stu-id="dd46a-128">-ApplicationObject</span></span>
<span data-ttu-id="dd46a-129">Obiekt aplikacji, którego główna usługa jest pobierana.</span><span class="sxs-lookup"><span data-stu-id="dd46a-129">The application object whose service principal is being retrieved.</span></span>

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

### <span data-ttu-id="dd46a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd46a-130">-DefaultProfile</span></span>
<span data-ttu-id="dd46a-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dd46a-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd46a-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dd46a-132">-DisplayName</span></span>
<span data-ttu-id="dd46a-133">Nazwa wyświetlana głównej usługi.</span><span class="sxs-lookup"><span data-stu-id="dd46a-133">The service principal display name.</span></span>

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

### <span data-ttu-id="dd46a-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="dd46a-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="dd46a-135">Ciąg wyszukiwania głównego usługi.</span><span class="sxs-lookup"><span data-stu-id="dd46a-135">The service principal search string.</span></span>

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

### <span data-ttu-id="dd46a-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dd46a-136">-ObjectId</span></span>
<span data-ttu-id="dd46a-137">Identyfikator obiektu głównego usługi.</span><span class="sxs-lookup"><span data-stu-id="dd46a-137">Object id of the service principal.</span></span>

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

### <span data-ttu-id="dd46a-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="dd46a-138">-ServicePrincipalName</span></span>
<span data-ttu-id="dd46a-139">SPN usługi.</span><span class="sxs-lookup"><span data-stu-id="dd46a-139">SPN of the service.</span></span>

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

### <span data-ttu-id="dd46a-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="dd46a-140">-IncludeTotalCount</span></span>
<span data-ttu-id="dd46a-141">Wyświetla liczbę obiektów w zbiorze danych.</span><span class="sxs-lookup"><span data-stu-id="dd46a-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="dd46a-142">Obecnie ten parametr nie wykonuje żadnych działań.</span><span class="sxs-lookup"><span data-stu-id="dd46a-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="dd46a-143">-Skip</span><span class="sxs-lookup"><span data-stu-id="dd46a-143">-Skip</span></span>
<span data-ttu-id="dd46a-144">Ignoruje pierwsze N obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="dd46a-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="dd46a-145">-First</span><span class="sxs-lookup"><span data-stu-id="dd46a-145">-First</span></span>
<span data-ttu-id="dd46a-146">Maksymalna liczba obiektów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="dd46a-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="dd46a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd46a-147">CommonParameters</span></span>
<span data-ttu-id="dd46a-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd46a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd46a-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd46a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd46a-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd46a-150">INPUTS</span></span>

### <span data-ttu-id="dd46a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="dd46a-151">System.String</span></span>

### <span data-ttu-id="dd46a-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="dd46a-152">System.Guid</span></span>

### <span data-ttu-id="dd46a-153">Microsoft. Azure. Commands. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="dd46a-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="dd46a-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd46a-154">OUTPUTS</span></span>

### <span data-ttu-id="dd46a-155">Microsoft. Azure. Commands. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dd46a-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="dd46a-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd46a-156">NOTES</span></span>

## <span data-ttu-id="dd46a-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd46a-157">RELATED LINKS</span></span>

[<span data-ttu-id="dd46a-158">Nowe — AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dd46a-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="dd46a-159">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dd46a-159">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="dd46a-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dd46a-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="dd46a-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="dd46a-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="dd46a-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="dd46a-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

