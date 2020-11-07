---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 2cb7455d5a902882fdd98dd5fea47ae5a28e1dc9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897289"
---
# <span data-ttu-id="9470a-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9470a-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="9470a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9470a-102">SYNOPSIS</span></span>
<span data-ttu-id="9470a-103">Tworzy konfigurację przekierowania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9470a-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9470a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9470a-104">SYNTAX</span></span>

### <span data-ttu-id="9470a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9470a-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9470a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9470a-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9470a-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="9470a-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9470a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9470a-108">DESCRIPTION</span></span>
<span data-ttu-id="9470a-109">Polecenie cmdlet **New-AzureRmApplicationGatewayRedirectConfiguration** umożliwia utworzenie konfiguracji przekierowywania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9470a-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="9470a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9470a-110">EXAMPLES</span></span>

### <span data-ttu-id="9470a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9470a-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="9470a-112">To polecenie tworzy konfigurację przekierowania o nazwie Redirect01 i zapisuje wynik w zmiennej o nazwie $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="9470a-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="9470a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9470a-113">PARAMETERS</span></span>

### <span data-ttu-id="9470a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9470a-114">-DefaultProfile</span></span>
<span data-ttu-id="9470a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9470a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9470a-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="9470a-116">-IncludePath</span></span>
<span data-ttu-id="9470a-117">Dołącz ścieżkę w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="9470a-117">Include path in the redirected url.</span></span>
<span data-ttu-id="9470a-118">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="9470a-118">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9470a-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="9470a-119">-IncludeQueryString</span></span>
<span data-ttu-id="9470a-120">Uwzględnij ciąg zapytania w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="9470a-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="9470a-121">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="9470a-121">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9470a-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9470a-122">-Name</span></span>
<span data-ttu-id="9470a-123">Nazwa konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="9470a-123">The name of the Redirect Configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9470a-124">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="9470a-124">-RedirectType</span></span>
<span data-ttu-id="9470a-125">Typ przekierowania</span><span class="sxs-lookup"><span data-stu-id="9470a-125">The type of redirect</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9470a-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="9470a-126">-TargetListener</span></span>
<span data-ttu-id="9470a-127">HTTPListener, aby przekierować żądanie do</span><span class="sxs-lookup"><span data-stu-id="9470a-127">HTTPListener to redirect the request to</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9470a-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="9470a-128">-TargetListenerID</span></span>
<span data-ttu-id="9470a-129">Identyfikator odbiornika, do którego ma zostać przekierowana prośba o</span><span class="sxs-lookup"><span data-stu-id="9470a-129">ID of  listener to redirect the request to</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9470a-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="9470a-130">-TargetUrl</span></span>
<span data-ttu-id="9470a-131">Docelowy adres URL, przekierowanie</span><span class="sxs-lookup"><span data-stu-id="9470a-131">Target URL fo redirection</span></span>

```yaml
Type: String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9470a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9470a-132">CommonParameters</span></span>
<span data-ttu-id="9470a-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9470a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9470a-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9470a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9470a-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9470a-135">INPUTS</span></span>

### <span data-ttu-id="9470a-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9470a-136">None</span></span>

## <span data-ttu-id="9470a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9470a-137">OUTPUTS</span></span>

### <span data-ttu-id="9470a-138">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9470a-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="9470a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9470a-139">NOTES</span></span>

## <span data-ttu-id="9470a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9470a-140">RELATED LINKS</span></span>

