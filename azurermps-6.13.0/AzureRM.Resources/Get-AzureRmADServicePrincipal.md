---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 983d5049d0ac58671b3d0766b6b4bcf3f05d4d76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544872"
---
# <span data-ttu-id="b9f44-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b9f44-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="b9f44-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9f44-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f44-103">Umożliwia filtrowanie podmiotów zabezpieczeń usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b9f44-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9f44-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9f44-104">SYNTAX</span></span>

### <span data-ttu-id="b9f44-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b9f44-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b9f44-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9f44-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b9f44-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9f44-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b9f44-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9f44-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b9f44-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9f44-109">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b9f44-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9f44-110">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b9f44-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9f44-111">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="b9f44-112">Opis</span><span class="sxs-lookup"><span data-stu-id="b9f44-112">DESCRIPTION</span></span>
<span data-ttu-id="b9f44-113">Umożliwia filtrowanie podmiotów zabezpieczeń usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b9f44-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="b9f44-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9f44-114">EXAMPLES</span></span>

### <span data-ttu-id="b9f44-115">Przykład 1-list podmiotów usługi AD</span><span class="sxs-lookup"><span data-stu-id="b9f44-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="b9f44-116">Wyświetla listę wszystkich podmiotów zabezpieczeń usługi AD w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="b9f44-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="b9f44-117">Przykład 2 — Wyświetlanie listy podmiotów zabezpieczeń usługi AD przy użyciu stronicowania</span><span class="sxs-lookup"><span data-stu-id="b9f44-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -First 100
```

<span data-ttu-id="b9f44-118">Wyświetla listę pierwszych 100 głównych usług REKLAMowych w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="b9f44-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="b9f44-119">Przykład 3-Wyświetlanie listy podmiotów nazw usług według nazwy SPN</span><span class="sxs-lookup"><span data-stu-id="b9f44-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="b9f44-120">Wyświetla listę podmiotów usługi za pomocą nazwy SPN "36f81fc3-b00f-48cd-8218-3879f51ff39f".</span><span class="sxs-lookup"><span data-stu-id="b9f44-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="b9f44-121">Przykład 4-Wyświetlanie listy głównych podmiotów usługi według ciągu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="b9f44-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="b9f44-122">Wyświetla listę wszystkich podmiotów nazw usługi AD, których nazwa wyświetlana rozpoczyna się od "Web".</span><span class="sxs-lookup"><span data-stu-id="b9f44-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="b9f44-123">Przykład 5-Wyświetlanie listy głównych usług według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="b9f44-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzureRmADServicePrincipal
```

<span data-ttu-id="b9f44-124">Pobiera aplikację reklamy o identyfikatorze obiektu "39e64ec6-569b-4030-8e1c-c3c519a05d69" i przekazuje ją do polecenia cmdlet Get-AzureRmADServicePrincipal, aby wyświetlić listę wszystkich głównych usług dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b9f44-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzureRmADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="b9f44-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9f44-125">PARAMETERS</span></span>

### <span data-ttu-id="b9f44-126">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="b9f44-126">-ApplicationId</span></span>
<span data-ttu-id="b9f44-127">Identyfikator głównej aplikacji usługi.</span><span class="sxs-lookup"><span data-stu-id="b9f44-127">The service principal application id.</span></span>

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

### <span data-ttu-id="b9f44-128">-Applicationobject</span><span class="sxs-lookup"><span data-stu-id="b9f44-128">-ApplicationObject</span></span>
<span data-ttu-id="b9f44-129">Obiekt aplikacji, którego główna usługa jest pobierana.</span><span class="sxs-lookup"><span data-stu-id="b9f44-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9f44-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9f44-130">-DefaultProfile</span></span>
<span data-ttu-id="b9f44-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b9f44-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9f44-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b9f44-132">-DisplayName</span></span>
<span data-ttu-id="b9f44-133">Nazwa wyświetlana głównej usługi.</span><span class="sxs-lookup"><span data-stu-id="b9f44-133">The service principal display name.</span></span>

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

### <span data-ttu-id="b9f44-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="b9f44-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="b9f44-135">Ciąg wyszukiwania głównego usługi.</span><span class="sxs-lookup"><span data-stu-id="b9f44-135">The service principal search string.</span></span>

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

### <span data-ttu-id="b9f44-136">-First</span><span class="sxs-lookup"><span data-stu-id="b9f44-136">-First</span></span>
<span data-ttu-id="b9f44-137">Maksymalna liczba obiektów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="b9f44-137">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="b9f44-138">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="b9f44-138">-IncludeTotalCount</span></span>
<span data-ttu-id="b9f44-139">Wyświetla liczbę obiektów w zbiorze danych.</span><span class="sxs-lookup"><span data-stu-id="b9f44-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="b9f44-140">Obecnie ten parametr nie wykonuje żadnych działań.</span><span class="sxs-lookup"><span data-stu-id="b9f44-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="b9f44-141">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b9f44-141">-ObjectId</span></span>
<span data-ttu-id="b9f44-142">Identyfikator obiektu głównego usługi.</span><span class="sxs-lookup"><span data-stu-id="b9f44-142">Object id of the service principal.</span></span>

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

### <span data-ttu-id="b9f44-143">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b9f44-143">-ServicePrincipalName</span></span>
<span data-ttu-id="b9f44-144">SPN usługi.</span><span class="sxs-lookup"><span data-stu-id="b9f44-144">SPN of the service.</span></span>

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

### <span data-ttu-id="b9f44-145">-Skip</span><span class="sxs-lookup"><span data-stu-id="b9f44-145">-Skip</span></span>
<span data-ttu-id="b9f44-146">Ignoruje pierwsze N obiektów, a następnie pobiera pozostałe obiekty.</span><span class="sxs-lookup"><span data-stu-id="b9f44-146">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="b9f44-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f44-147">CommonParameters</span></span>
<span data-ttu-id="b9f44-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9f44-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f44-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9f44-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f44-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9f44-150">INPUTS</span></span>

### <span data-ttu-id="b9f44-151">System. String</span><span class="sxs-lookup"><span data-stu-id="b9f44-151">System.String</span></span>

### <span data-ttu-id="b9f44-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b9f44-152">System.Guid</span></span>

### <span data-ttu-id="b9f44-153">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="b9f44-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="b9f44-154">Parametry: Applicationobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b9f44-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="b9f44-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9f44-155">OUTPUTS</span></span>

### <span data-ttu-id="b9f44-156">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b9f44-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="b9f44-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9f44-157">NOTES</span></span>

## <span data-ttu-id="b9f44-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9f44-158">RELATED LINKS</span></span>

[<span data-ttu-id="b9f44-159">Nowe — AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b9f44-159">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b9f44-160">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b9f44-160">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b9f44-161">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b9f44-161">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b9f44-162">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b9f44-162">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="b9f44-163">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b9f44-163">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

