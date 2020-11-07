---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: c5276ddbcd10870355f8530c2f04f81122dda382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717165"
---
# <span data-ttu-id="7dc51-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7dc51-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="7dc51-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7dc51-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc51-103">Wyświetla istniejące aplikacje usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7dc51-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dc51-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7dc51-104">SYNTAX</span></span>

### <span data-ttu-id="7dc51-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7dc51-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dc51-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dc51-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dc51-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dc51-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dc51-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dc51-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7dc51-109">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dc51-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7dc51-110">Opis</span><span class="sxs-lookup"><span data-stu-id="7dc51-110">DESCRIPTION</span></span>
<span data-ttu-id="7dc51-111">Wyświetla istniejące aplikacje usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7dc51-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="7dc51-112">Wyszukiwanie aplikacji można przeprowadzić przez ObjectId, identyfikator aplikacji, IdentifierUri lub DisplayName.</span><span class="sxs-lookup"><span data-stu-id="7dc51-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="7dc51-113">Jeśli nie podano parametru, pobiera wszystkie aplikacje w ramach dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="7dc51-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="7dc51-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7dc51-114">EXAMPLES</span></span>

### <span data-ttu-id="7dc51-115">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7dc51-115">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="7dc51-116">Wyświetla listę wszystkich aplikacji w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="7dc51-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="7dc51-117">--------------------------Przykład 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7dc51-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="7dc51-118">Pobiera aplikację o identyfikatorze URI " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="7dc51-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="7dc51-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7dc51-119">PARAMETERS</span></span>

### <span data-ttu-id="7dc51-120">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="7dc51-120">-ApplicationId</span></span>
<span data-ttu-id="7dc51-121">Identyfikator aplikacji, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="7dc51-121">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="7dc51-122">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="7dc51-122">-DisplayNameStartWith</span></span>
<span data-ttu-id="7dc51-123">Pobierz wszystkie aplikacje, rozpoczynając od nazwy wyświetlanej.</span><span class="sxs-lookup"><span data-stu-id="7dc51-123">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dc51-124">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="7dc51-124">-IdentifierUri</span></span>
<span data-ttu-id="7dc51-125">Unikatowy identyfikator identyfikator URI aplikacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="7dc51-125">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="7dc51-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7dc51-126">-ObjectId</span></span>
<span data-ttu-id="7dc51-127">Identyfikator obiektu aplikacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="7dc51-127">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="7dc51-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc51-128">-DefaultProfile</span></span>
<span data-ttu-id="7dc51-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7dc51-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dc51-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc51-130">CommonParameters</span></span>
<span data-ttu-id="7dc51-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dc51-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc51-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dc51-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc51-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dc51-133">INPUTS</span></span>

## <span data-ttu-id="7dc51-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7dc51-134">OUTPUTS</span></span>

### <span data-ttu-id="7dc51-135">System. Collections. Generic. list "1 [Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication]</span><span class="sxs-lookup"><span data-stu-id="7dc51-135">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="7dc51-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7dc51-136">NOTES</span></span>

## <span data-ttu-id="7dc51-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7dc51-137">RELATED LINKS</span></span>

[<span data-ttu-id="7dc51-138">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7dc51-138">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="7dc51-139">Nowe — AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7dc51-139">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="7dc51-140">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7dc51-140">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="7dc51-141">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7dc51-141">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="7dc51-142">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7dc51-142">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="7dc51-143">Nowe — AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7dc51-143">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

