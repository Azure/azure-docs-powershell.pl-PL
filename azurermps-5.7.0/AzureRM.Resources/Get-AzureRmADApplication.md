---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: b44d3bbf7c594f5f9114488b536d28fd17fe56c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550584"
---
# <span data-ttu-id="e400f-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e400f-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="e400f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e400f-102">SYNOPSIS</span></span>
<span data-ttu-id="e400f-103">Wyświetla istniejące aplikacje usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e400f-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e400f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e400f-104">SYNTAX</span></span>

### <span data-ttu-id="e400f-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e400f-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e400f-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e400f-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e400f-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e400f-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e400f-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e400f-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e400f-109">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="e400f-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e400f-110">Opis</span><span class="sxs-lookup"><span data-stu-id="e400f-110">DESCRIPTION</span></span>
<span data-ttu-id="e400f-111">Wyświetla istniejące aplikacje usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e400f-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="e400f-112">Wyszukiwanie aplikacji można przeprowadzić przez ObjectId, identyfikator aplikacji, IdentifierUri lub DisplayName.</span><span class="sxs-lookup"><span data-stu-id="e400f-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="e400f-113">Jeśli nie podano parametru, pobiera wszystkie aplikacje w ramach dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e400f-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="e400f-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e400f-114">EXAMPLES</span></span>

### <span data-ttu-id="e400f-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e400f-115">Example 1</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="e400f-116">Wyświetla listę wszystkich aplikacji w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="e400f-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="e400f-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e400f-117">Example 2</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="e400f-118">Pobiera aplikację o identyfikatorze URI " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="e400f-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="e400f-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e400f-119">PARAMETERS</span></span>

### <span data-ttu-id="e400f-120">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="e400f-120">-ApplicationId</span></span>
<span data-ttu-id="e400f-121">Identyfikator aplikacji, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="e400f-121">The application id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e400f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e400f-122">-DefaultProfile</span></span>
<span data-ttu-id="e400f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e400f-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e400f-124">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="e400f-124">-DisplayNameStartWith</span></span>
<span data-ttu-id="e400f-125">Pobierz wszystkie aplikacje, rozpoczynając od nazwy wyświetlanej.</span><span class="sxs-lookup"><span data-stu-id="e400f-125">Fetch all applications starting with the display name.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e400f-126">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="e400f-126">-IdentifierUri</span></span>
<span data-ttu-id="e400f-127">Unikatowy identyfikator identyfikator URI aplikacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="e400f-127">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e400f-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e400f-128">-ObjectId</span></span>
<span data-ttu-id="e400f-129">Identyfikator obiektu aplikacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="e400f-129">The object id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e400f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e400f-130">CommonParameters</span></span>
<span data-ttu-id="e400f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e400f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e400f-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e400f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e400f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e400f-133">INPUTS</span></span>

### <span data-ttu-id="e400f-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e400f-134">None</span></span>
<span data-ttu-id="e400f-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e400f-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e400f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e400f-136">OUTPUTS</span></span>

### <span data-ttu-id="e400f-137">System. Collections. Generic. list "1 [Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication]</span><span class="sxs-lookup"><span data-stu-id="e400f-137">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="e400f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e400f-138">NOTES</span></span>

## <span data-ttu-id="e400f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e400f-139">RELATED LINKS</span></span>

[<span data-ttu-id="e400f-140">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e400f-140">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="e400f-141">Nowe — AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e400f-141">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="e400f-142">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e400f-142">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="e400f-143">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e400f-143">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="e400f-144">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e400f-144">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="e400f-145">Nowe — AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e400f-145">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

