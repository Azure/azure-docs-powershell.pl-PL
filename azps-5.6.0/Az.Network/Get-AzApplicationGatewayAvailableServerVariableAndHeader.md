---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: f4f2e76a9354ee6ed796b64cbdd83f21d70ff954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978385"
---
# <span data-ttu-id="17c6c-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="17c6c-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="17c6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="17c6c-103">Pobierz obsługiwane zmienne serwera oraz dostępne nagłówki żądań i odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="17c6c-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="17c6c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="17c6c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="17c6c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="17c6c-105">DESCRIPTION</span></span>
<span data-ttu-id="17c6c-106">Polecenie **cmdlet Get-AzApplicationGatewayAvailableServerVariableAndHeader** pobiera obsługiwane zmienne serwera oraz dostępne nagłówki żądań i odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="17c6c-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="17c6c-107">Parametry mogą być używane do odejmowania zmiennych lub list nagłówków.</span><span class="sxs-lookup"><span data-stu-id="17c6c-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="17c6c-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="17c6c-108">EXAMPLES</span></span>

### <span data-ttu-id="17c6c-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="17c6c-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="17c6c-110">To polecenia zwraca wszystkie dostępne zmienne serwera.</span><span class="sxs-lookup"><span data-stu-id="17c6c-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="17c6c-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="17c6c-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="17c6c-112">To polecenia zwraca wszystkie dostępne nagłówki żądań.</span><span class="sxs-lookup"><span data-stu-id="17c6c-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="17c6c-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="17c6c-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="17c6c-114">To polecenia zwraca wszystkie dostępne nagłówki odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="17c6c-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="17c6c-115">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="17c6c-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="17c6c-116">To polecenia zwraca wszystkie dostępne zmienne serwera, nagłówki żądań i odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="17c6c-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="17c6c-117">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="17c6c-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="17c6c-118">To polecenia zwraca wszystkie dostępne zmienne serwera, nagłówki żądań i odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="17c6c-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="17c6c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17c6c-119">PARAMETERS</span></span>

### <span data-ttu-id="17c6c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17c6c-120">-DefaultProfile</span></span>
<span data-ttu-id="17c6c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="17c6c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17c6c-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="17c6c-122">-RequestHeader</span></span>
<span data-ttu-id="17c6c-123">Dostępne nagłówki żądań bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="17c6c-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="17c6c-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="17c6c-124">-ResponseHeader</span></span>
<span data-ttu-id="17c6c-125">Brama aplikacji zawiera nagłówki odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="17c6c-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="17c6c-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="17c6c-126">-ServerVariable</span></span>
<span data-ttu-id="17c6c-127">Dostępne zmienne serwera bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="17c6c-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="17c6c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17c6c-128">CommonParameters</span></span>
<span data-ttu-id="17c6c-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17c6c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17c6c-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17c6c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17c6c-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17c6c-131">INPUTS</span></span>

### <span data-ttu-id="17c6c-132">Brak</span><span class="sxs-lookup"><span data-stu-id="17c6c-132">None</span></span>

## <span data-ttu-id="17c6c-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17c6c-133">OUTPUTS</span></span>

### <span data-ttu-id="17c6c-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="17c6c-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="17c6c-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="17c6c-135">NOTES</span></span>
<span data-ttu-id="17c6c-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** to alias polecenia cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader.**</span><span class="sxs-lookup"><span data-stu-id="17c6c-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="17c6c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17c6c-137">RELATED LINKS</span></span>
