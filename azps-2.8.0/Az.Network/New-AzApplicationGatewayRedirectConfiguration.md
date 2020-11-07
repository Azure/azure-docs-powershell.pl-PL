---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: e768c8f5e557954dd6e932726f38b9844699de9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870524"
---
# <span data-ttu-id="9d8aa-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d8aa-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="9d8aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="9d8aa-103">Tworzy konfigurację przekierowania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9d8aa-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="9d8aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d8aa-104">SYNTAX</span></span>

### <span data-ttu-id="9d8aa-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d8aa-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d8aa-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9d8aa-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d8aa-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="9d8aa-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d8aa-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9d8aa-108">DESCRIPTION</span></span>
<span data-ttu-id="9d8aa-109">Polecenie cmdlet **New-AzApplicationGatewayRedirectConfiguration** umożliwia utworzenie konfiguracji przekierowywania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9d8aa-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="9d8aa-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d8aa-110">EXAMPLES</span></span>

### <span data-ttu-id="9d8aa-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9d8aa-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="9d8aa-112">To polecenie tworzy konfigurację przekierowania o nazwie Redirect01 i zapisuje wynik w zmiennej o nazwie $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="9d8aa-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="9d8aa-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d8aa-113">PARAMETERS</span></span>

### <span data-ttu-id="9d8aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d8aa-114">-DefaultProfile</span></span>
<span data-ttu-id="9d8aa-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d8aa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d8aa-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="9d8aa-116">-IncludePath</span></span>
<span data-ttu-id="9d8aa-117">Dołącz ścieżkę w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="9d8aa-117">Include path in the redirected url.</span></span>
<span data-ttu-id="9d8aa-118">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="9d8aa-118">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d8aa-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="9d8aa-119">-IncludeQueryString</span></span>
<span data-ttu-id="9d8aa-120">Uwzględnij ciąg zapytania w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="9d8aa-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="9d8aa-121">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="9d8aa-121">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d8aa-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9d8aa-122">-Name</span></span>
<span data-ttu-id="9d8aa-123">Nazwa konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="9d8aa-123">The name of the Redirect Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d8aa-124">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="9d8aa-124">-RedirectType</span></span>
<span data-ttu-id="9d8aa-125">Typ przekierowania</span><span class="sxs-lookup"><span data-stu-id="9d8aa-125">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d8aa-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="9d8aa-126">-TargetListener</span></span>
<span data-ttu-id="9d8aa-127">Odbiornik HTTP umożliwiający przekierowanie żądania do</span><span class="sxs-lookup"><span data-stu-id="9d8aa-127">HTTP listener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d8aa-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="9d8aa-128">-TargetListenerID</span></span>
<span data-ttu-id="9d8aa-129">Identyfikator odbiornika HTTP do przekierowania żądania do</span><span class="sxs-lookup"><span data-stu-id="9d8aa-129">ID of HTTP listener to redirect the request to</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d8aa-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="9d8aa-130">-TargetUrl</span></span>
<span data-ttu-id="9d8aa-131">Docelowy adres URL, przekierowanie</span><span class="sxs-lookup"><span data-stu-id="9d8aa-131">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d8aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d8aa-132">CommonParameters</span></span>
<span data-ttu-id="9d8aa-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d8aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d8aa-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d8aa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d8aa-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d8aa-135">INPUTS</span></span>

### <span data-ttu-id="9d8aa-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9d8aa-136">None</span></span>

## <span data-ttu-id="9d8aa-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d8aa-137">OUTPUTS</span></span>

### <span data-ttu-id="9d8aa-138">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d8aa-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="9d8aa-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d8aa-139">NOTES</span></span>

## <span data-ttu-id="9d8aa-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d8aa-140">RELATED LINKS</span></span>

[<span data-ttu-id="9d8aa-141">Dodaj-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d8aa-141">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="9d8aa-142">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d8aa-142">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="9d8aa-143">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d8aa-143">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="9d8aa-144">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d8aa-144">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
