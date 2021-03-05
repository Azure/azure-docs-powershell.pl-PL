---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionsignatureoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
ms.openlocfilehash: c6aa2bb9bf3866e35ad59e59bdf5ded333fd2816
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011882"
---
# <span data-ttu-id="94c9a-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="94c9a-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="94c9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="94c9a-103">Tworzy nowe zastępowanie podpisu wykrywania intruzów zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="94c9a-103">Creates a new Azure Firewall Policy Intrusion Detection Signature Override</span></span>

## <span data-ttu-id="94c9a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="94c9a-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id <UInt64> -Mode <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94c9a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="94c9a-105">DESCRIPTION</span></span>
<span data-ttu-id="94c9a-106">Polecenie **cmdlet New-AzFirewallPolicyIntrusionDetectionSignatureOverride** tworzy obiekt zastępowania podpisu zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="94c9a-106">The **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cmdlet creates an Azure Firewall Policy Signature Override Object.</span></span>

## <span data-ttu-id="94c9a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="94c9a-107">EXAMPLES</span></span>

### <span data-ttu-id="94c9a-108">Przykład 1: 1.</span><span class="sxs-lookup"><span data-stu-id="94c9a-108">Example 1: 1.</span></span> <span data-ttu-id="94c9a-109">Tworzenie wykrywania włamań za pomocą zastępować podpisu</span><span class="sxs-lookup"><span data-stu-id="94c9a-109">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```
<span data-ttu-id="94c9a-110">W tym przykładzie jest konstruowanie wykrywania dostępu z określonym zastąpieniem podpisu w trybie Odmów</span><span class="sxs-lookup"><span data-stu-id="94c9a-110">This example creates intrusion detection with specific signature override to Deny mode</span></span>

## <span data-ttu-id="94c9a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94c9a-111">PARAMETERS</span></span>

### <span data-ttu-id="94c9a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c9a-112">-DefaultProfile</span></span>
<span data-ttu-id="94c9a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="94c9a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c9a-114">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="94c9a-114">-Id</span></span>
<span data-ttu-id="94c9a-115">Identyfikator podpisu.</span><span class="sxs-lookup"><span data-stu-id="94c9a-115">Signature id.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c9a-116">— tryb</span><span class="sxs-lookup"><span data-stu-id="94c9a-116">-Mode</span></span>
<span data-ttu-id="94c9a-117">Stan podpisu.</span><span class="sxs-lookup"><span data-stu-id="94c9a-117">Signature state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Off, Alert, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c9a-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94c9a-118">-Confirm</span></span>
<span data-ttu-id="94c9a-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="94c9a-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c9a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94c9a-120">-WhatIf</span></span>
<span data-ttu-id="94c9a-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94c9a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94c9a-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="94c9a-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c9a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c9a-123">CommonParameters</span></span>
<span data-ttu-id="94c9a-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94c9a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c9a-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94c9a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c9a-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94c9a-126">INPUTS</span></span>

### <span data-ttu-id="94c9a-127">Brak</span><span class="sxs-lookup"><span data-stu-id="94c9a-127">None</span></span>

## <span data-ttu-id="94c9a-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94c9a-128">OUTPUTS</span></span>

### <span data-ttu-id="94c9a-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="94c9a-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="94c9a-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="94c9a-130">NOTES</span></span>

## <span data-ttu-id="94c9a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94c9a-131">RELATED LINKS</span></span>
