---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8fb1f76b32332c7679ef59f50123072311de86fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499614"
---
# <span data-ttu-id="6c93d-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="6c93d-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="6c93d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c93d-102">SYNOPSIS</span></span>
<span data-ttu-id="6c93d-103">Uzyskaj obsługiwane zmienne serwerowe i dostępne nagłówki żądań i odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="6c93d-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="6c93d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c93d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="6c93d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6c93d-105">DESCRIPTION</span></span>
<span data-ttu-id="6c93d-106">Polecenie cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** pobiera obsługiwane zmienne serwerowe oraz dostępne nagłówki żądań i odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="6c93d-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="6c93d-107">Za pomocą parametrów można uzyskać listy zmiennych i nagłówków.</span><span class="sxs-lookup"><span data-stu-id="6c93d-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="6c93d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c93d-108">EXAMPLES</span></span>

### <span data-ttu-id="6c93d-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c93d-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="6c93d-110">To polecenie zwraca wszystkie dostępne zmienne serwerowe.</span><span class="sxs-lookup"><span data-stu-id="6c93d-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="6c93d-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6c93d-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="6c93d-112">To polecenie zwraca wszystkie dostępne nagłówki żądań.</span><span class="sxs-lookup"><span data-stu-id="6c93d-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="6c93d-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="6c93d-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="6c93d-114">To polecenie zwraca wszystkie dostępne nagłówki odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="6c93d-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="6c93d-115">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="6c93d-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="6c93d-116">To polecenie zwraca wszystkie dostępne zmienne serwerowe, nagłówki żądań i odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="6c93d-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="6c93d-117">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="6c93d-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="6c93d-118">To polecenie zwraca wszystkie dostępne zmienne serwerowe, nagłówki żądań i odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="6c93d-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="6c93d-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c93d-119">PARAMETERS</span></span>

### <span data-ttu-id="6c93d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c93d-120">-DefaultProfile</span></span>
<span data-ttu-id="6c93d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c93d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c93d-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="6c93d-122">-RequestHeader</span></span>
<span data-ttu-id="6c93d-123">Nagłówki żądań dostępne w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6c93d-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="6c93d-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="6c93d-124">-ResponseHeader</span></span>
<span data-ttu-id="6c93d-125">Nagłówki odpowiedzi dostępne w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6c93d-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="6c93d-126">-ServerVariables</span><span class="sxs-lookup"><span data-stu-id="6c93d-126">-ServerVariable</span></span>
<span data-ttu-id="6c93d-127">Zmienne serwerowe dostępne w bramie Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6c93d-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="6c93d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c93d-128">CommonParameters</span></span>
<span data-ttu-id="6c93d-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c93d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c93d-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c93d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c93d-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c93d-131">INPUTS</span></span>

### <span data-ttu-id="6c93d-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6c93d-132">None</span></span>

## <span data-ttu-id="6c93d-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c93d-133">OUTPUTS</span></span>

### <span data-ttu-id="6c93d-134">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="6c93d-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="6c93d-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c93d-135">NOTES</span></span>
<span data-ttu-id="6c93d-136">**Lista — AzApplicationGatewayAvailableServerVariableAndHeader** to alias polecenia cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** .</span><span class="sxs-lookup"><span data-stu-id="6c93d-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="6c93d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c93d-137">RELATED LINKS</span></span>
