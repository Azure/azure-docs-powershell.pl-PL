---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9fae8c6d543bddc3ad4110b95a1c1b4a1f146879
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193594"
---
# <span data-ttu-id="4662e-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="4662e-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="4662e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4662e-102">SYNOPSIS</span></span>
<span data-ttu-id="4662e-103">Zdefiniuj nowe zasady podziału ruchu usługi Office 365, które będą używane z witryną urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="4662e-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="4662e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4662e-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4662e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4662e-105">DESCRIPTION</span></span>
<span data-ttu-id="4662e-106">Polecenie New-AzOffice365PolicyProperties określa zasady podziału usługi Office 365, które mają być używane z witryną wirtualnego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="4662e-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="4662e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4662e-107">EXAMPLES</span></span>

### <span data-ttu-id="4662e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4662e-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="4662e-109">Utwórz obiekt zasad podziału ruchu usługi Office 365, który będzie używany z poleceniami witryny Wirtualne urządzenie.</span><span class="sxs-lookup"><span data-stu-id="4662e-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="4662e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4662e-110">PARAMETERS</span></span>

### <span data-ttu-id="4662e-111">— Zezwalaj</span><span class="sxs-lookup"><span data-stu-id="4662e-111">-Allow</span></span>
<span data-ttu-id="4662e-112">Rozbijanie ruchu kategorii zezwalaj na.</span><span class="sxs-lookup"><span data-stu-id="4662e-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="4662e-113">— Domyślne</span><span class="sxs-lookup"><span data-stu-id="4662e-113">-Default</span></span>
<span data-ttu-id="4662e-114">Rozbijanie domyślnego ruchu kategorii.</span><span class="sxs-lookup"><span data-stu-id="4662e-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="4662e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4662e-115">-DefaultProfile</span></span>
<span data-ttu-id="4662e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4662e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4662e-117">— Optymalizowanie</span><span class="sxs-lookup"><span data-stu-id="4662e-117">-Optimize</span></span>
<span data-ttu-id="4662e-118">Rozbijanie ruchu kategorii optymalizowania.</span><span class="sxs-lookup"><span data-stu-id="4662e-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="4662e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4662e-119">CommonParameters</span></span>
<span data-ttu-id="4662e-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4662e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4662e-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4662e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4662e-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4662e-122">INPUTS</span></span>

### <span data-ttu-id="4662e-123">Brak</span><span class="sxs-lookup"><span data-stu-id="4662e-123">None</span></span>

## <span data-ttu-id="4662e-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4662e-124">OUTPUTS</span></span>

### <span data-ttu-id="4662e-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="4662e-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="4662e-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4662e-126">NOTES</span></span>

## <span data-ttu-id="4662e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4662e-127">RELATED LINKS</span></span>
