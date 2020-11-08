---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: b1665975fd85268bdb8788eb96ba0c8694b6f4c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053776"
---
# <span data-ttu-id="a4329-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="a4329-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="a4329-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4329-102">SYNOPSIS</span></span>
<span data-ttu-id="a4329-103">Tworzy ustawienie zasad dla zasad zapory</span><span class="sxs-lookup"><span data-stu-id="a4329-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="a4329-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4329-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4329-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a4329-105">DESCRIPTION</span></span>
<span data-ttu-id="a4329-106">**Nowe-AzApplicationGatewayFirewallPolicySetting** tworzy ustawienia zasad dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="a4329-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="a4329-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4329-107">EXAMPLES</span></span>

### <span data-ttu-id="a4329-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4329-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="a4329-109">Polecenie tworzy ustawienie zasad ze stanem $enabledState, Mode as $enabledMode, RequestBodyCheck jako FAŁSZ, FileUploadLimitInMb jako $fileUploadLimitInMb i MaxRequestBodySizeInKb jako $ $maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="a4329-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="a4329-110">Nowy policySettings jest przechowywany w $condition.</span><span class="sxs-lookup"><span data-stu-id="a4329-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="a4329-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4329-111">PARAMETERS</span></span>

### <span data-ttu-id="a4329-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4329-112">-DefaultProfile</span></span>
<span data-ttu-id="a4329-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4329-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4329-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="a4329-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="a4329-115">RequestBodyCheck w ustawieniach zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="a4329-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="a4329-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="a4329-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="a4329-117">Maksymalny rozmiar fileUpload w MB.</span><span class="sxs-lookup"><span data-stu-id="a4329-117">Maximum fileUpload size in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4329-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="a4329-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="a4329-119">MaxRequestBodySizeInKb w ustawieniach zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="a4329-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 128
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4329-120">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="a4329-120">-Mode</span></span>
<span data-ttu-id="a4329-121">Tryb zapory w ustawieniach zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="a4329-121">Firewall Mode in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: Detection
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4329-122">-State</span><span class="sxs-lookup"><span data-stu-id="a4329-122">-State</span></span>
<span data-ttu-id="a4329-123">Zmienna State w ustawieniach zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="a4329-123">State variable in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4329-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4329-124">CommonParameters</span></span>
<span data-ttu-id="a4329-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4329-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4329-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4329-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4329-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4329-127">INPUTS</span></span>

### <span data-ttu-id="a4329-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a4329-128">None</span></span>

## <span data-ttu-id="a4329-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4329-129">OUTPUTS</span></span>

### <span data-ttu-id="a4329-130">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="a4329-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="a4329-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4329-131">NOTES</span></span>

## <span data-ttu-id="a4329-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4329-132">RELATED LINKS</span></span>
