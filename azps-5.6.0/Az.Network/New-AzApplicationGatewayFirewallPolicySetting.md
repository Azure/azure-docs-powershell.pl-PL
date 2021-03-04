---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: 256509a42b844b196728b89b30abcdb6c5b9b386
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962737"
---
# <span data-ttu-id="964d7-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="964d7-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="964d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="964d7-102">SYNOPSIS</span></span>
<span data-ttu-id="964d7-103">Tworzy ustawienie zasad dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="964d7-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="964d7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="964d7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="964d7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="964d7-105">DESCRIPTION</span></span>
<span data-ttu-id="964d7-106">Ustawienie **New-AzApplicationGatewayFirewallPolicySetting** tworzy ustawienia zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="964d7-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="964d7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="964d7-107">EXAMPLES</span></span>

### <span data-ttu-id="964d7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="964d7-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="964d7-109">Polecenie tworzy ustawienie zasad o stanie $enabledState, tryb jako $enabledMode, RequestBodyCheck jako fałsz, FileUploadLimitInMb jako $fileUploadLimitInMb i MaxRequestBodySizeInKb jako $$maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="964d7-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="964d7-110">Nowe ustawienia zasad są przechowywane w $condition.</span><span class="sxs-lookup"><span data-stu-id="964d7-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="964d7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="964d7-111">PARAMETERS</span></span>

### <span data-ttu-id="964d7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="964d7-112">-DefaultProfile</span></span>
<span data-ttu-id="964d7-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="964d7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="964d7-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="964d7-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="964d7-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span><span class="sxs-lookup"><span data-stu-id="964d7-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="964d7-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="964d7-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="964d7-117">Maksymalny rozmiar plikuŁaduj w MB.</span><span class="sxs-lookup"><span data-stu-id="964d7-117">Maximum fileUpload size in MB.</span></span>

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

### <span data-ttu-id="964d7-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="964d7-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="964d7-119">MaxRequestBodySizeInKb w ustawieniach zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="964d7-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="964d7-120">— tryb</span><span class="sxs-lookup"><span data-stu-id="964d7-120">-Mode</span></span>
<span data-ttu-id="964d7-121">Tryb zapory w ustawieniach zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="964d7-121">Firewall Mode in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="964d7-122">— województwo</span><span class="sxs-lookup"><span data-stu-id="964d7-122">-State</span></span>
<span data-ttu-id="964d7-123">Zmienna województwa w ustawieniach zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="964d7-123">State variable in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="964d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="964d7-124">CommonParameters</span></span>
<span data-ttu-id="964d7-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="964d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="964d7-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="964d7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="964d7-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="964d7-127">INPUTS</span></span>

### <span data-ttu-id="964d7-128">Brak</span><span class="sxs-lookup"><span data-stu-id="964d7-128">None</span></span>

## <span data-ttu-id="964d7-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="964d7-129">OUTPUTS</span></span>

### <span data-ttu-id="964d7-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="964d7-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="964d7-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="964d7-131">NOTES</span></span>

## <span data-ttu-id="964d7-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="964d7-132">RELATED LINKS</span></span>
