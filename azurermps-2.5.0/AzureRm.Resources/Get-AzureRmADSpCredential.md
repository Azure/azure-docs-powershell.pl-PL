---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadspcredential
schema: 2.0.0
ms.openlocfilehash: a0f4c41b310e820b939500b8496b411d7b0266d1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898683"
---
# <span data-ttu-id="581a5-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="581a5-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="581a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="581a5-102">SYNOPSIS</span></span>
<span data-ttu-id="581a5-103">Pobiera listę poświadczeń skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="581a5-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="581a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="581a5-104">SYNTAX</span></span>

### <span data-ttu-id="581a5-105">ObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="581a5-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="581a5-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="581a5-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="581a5-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="581a5-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="581a5-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="581a5-108">SPNObjectParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="581a5-109">Opis</span><span class="sxs-lookup"><span data-stu-id="581a5-109">DESCRIPTION</span></span>
<span data-ttu-id="581a5-110">Polecenie cmdlet Get-AzureRmADSpCredential może służyć do pobierania listy poświadczeń skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="581a5-110">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="581a5-111">To polecenie spowoduje pobranie wszystkich właściwości poświadczeń (ale nie wartości poświadczeń) skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="581a5-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="581a5-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="581a5-112">EXAMPLES</span></span>

### <span data-ttu-id="581a5-113">Przykład 1-listowe poświadczenia według nazwy SPN</span><span class="sxs-lookup"><span data-stu-id="581a5-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="581a5-114">Zwraca listę poświadczeń skojarzonych z podmiotem zabezpieczeń usługi z główną wersją SPN http://test12345 .</span><span class="sxs-lookup"><span data-stu-id="581a5-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="581a5-115">Przykład 2-Wyświetlanie listy poświadczeń według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="581a5-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzureRmADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="581a5-116">Zwraca listę poświadczeń skojarzonych z podmiotem zabezpieczeń usługi o identyfikatorze obiektu "58e28616-99cc-4da4-b705-7672130e1047".</span><span class="sxs-lookup"><span data-stu-id="581a5-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="581a5-117">Przykład 3-Wyświetlaj poświadczenia według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="581a5-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzureRmADSpCredential
```

<span data-ttu-id="581a5-118">Pobiera podmiot zabezpieczeń usługi o identyfikatorze obiektu "58e28616-99cc-4da4-b705-7672130e1047" i przekazuje go do polecenia cmdlet Get-AzureRmADSpCredential, aby wyświetlić wszystkie poświadczenia dla tego podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="581a5-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzureRmADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="581a5-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="581a5-119">PARAMETERS</span></span>

### <span data-ttu-id="581a5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="581a5-120">-DefaultProfile</span></span>
<span data-ttu-id="581a5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="581a5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="581a5-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="581a5-122">-DisplayName</span></span>
<span data-ttu-id="581a5-123">Nazwa wyświetlana podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="581a5-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="581a5-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="581a5-124">-ObjectId</span></span>
<span data-ttu-id="581a5-125">Identyfikator obiektu podmiotu usługi, z którego mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="581a5-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581a5-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="581a5-126">-ServicePrincipalName</span></span>
<span data-ttu-id="581a5-127">Nazwa (SPN) podmiotu zabezpieczeń usługi, z którego mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="581a5-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581a5-128">-Serviceprincipalobject</span><span class="sxs-lookup"><span data-stu-id="581a5-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="581a5-129">Obiekt główny usługi, z którego mają zostać pobrane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="581a5-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="581a5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="581a5-130">CommonParameters</span></span>
<span data-ttu-id="581a5-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="581a5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="581a5-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="581a5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="581a5-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="581a5-133">INPUTS</span></span>

### <span data-ttu-id="581a5-134">System. GUID</span><span class="sxs-lookup"><span data-stu-id="581a5-134">System.Guid</span></span>

### <span data-ttu-id="581a5-135">System. String</span><span class="sxs-lookup"><span data-stu-id="581a5-135">System.String</span></span>

### <span data-ttu-id="581a5-136">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="581a5-136">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="581a5-137">Parametry: serviceprincipalobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="581a5-137">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="581a5-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="581a5-138">OUTPUTS</span></span>

### <span data-ttu-id="581a5-139">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="581a5-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="581a5-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="581a5-140">NOTES</span></span>

## <span data-ttu-id="581a5-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="581a5-141">RELATED LINKS</span></span>

[<span data-ttu-id="581a5-142">Nowe — AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="581a5-142">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="581a5-143">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="581a5-143">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="581a5-144">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="581a5-144">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

