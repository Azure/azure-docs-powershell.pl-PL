---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: 9d36169439a2466ca50858f5b438822461259cf3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318835"
---
# <span data-ttu-id="33836-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="33836-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="33836-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33836-102">SYNOPSIS</span></span>
<span data-ttu-id="33836-103">Pobiera grupę VM/serwer w formancie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="33836-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="33836-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33836-104">SYNTAX</span></span>

### <span data-ttu-id="33836-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="33836-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33836-106">Opis</span><span class="sxs-lookup"><span data-stu-id="33836-106">DESCRIPTION</span></span>
<span data-ttu-id="33836-107">Kontrolki aplikacji adaptacyjnych są obliczane automatycznie przez usługę Azure Security Center, użyj tego polecenia cmdlet, aby uzyskać grupę obiektów VM/serwer w formancie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="33836-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="33836-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33836-108">EXAMPLES</span></span>

### <span data-ttu-id="33836-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="33836-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="33836-110">Pobiera grupę VM/serwer w formancie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="33836-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="33836-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33836-111">PARAMETERS</span></span>

### <span data-ttu-id="33836-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33836-112">-DefaultProfile</span></span>
<span data-ttu-id="33836-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="33836-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33836-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="33836-114">-AscLocation</span></span>
<span data-ttu-id="33836-115">Miejsce, w którym są przechowywane dane subskrypcji w polu ASC.</span><span class="sxs-lookup"><span data-stu-id="33836-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="33836-116">można pobrać z lokalizacji Uzyskaj lokalizacje.</span><span class="sxs-lookup"><span data-stu-id="33836-116">can be retrieved from Get locations.</span></span>

```yaml
Type: System.String
Parameter Sets: AscLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33836-117">-GroupName</span><span class="sxs-lookup"><span data-stu-id="33836-117">-GroupName</span></span>
<span data-ttu-id="33836-118">Nazwa grupy kontrolek VM/serwer w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="33836-118">Name of an application control VM/server group.</span></span>

```yaml
Type: System.String
Parameter Sets: GroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33836-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="33836-119">-SubscriptionId</span></span>
<span data-ttu-id="33836-120">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="33836-120">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="33836-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33836-121">CommonParameters</span></span>
<span data-ttu-id="33836-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33836-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33836-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33836-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33836-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33836-124">INPUTS</span></span>

### <span data-ttu-id="33836-125">System. String</span><span class="sxs-lookup"><span data-stu-id="33836-125">System.String</span></span>

## <span data-ttu-id="33836-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33836-126">OUTPUTS</span></span>

### <span data-ttu-id="33836-127">Microsoft. Azure. Commands. Security. models. AdaptiveApplicationControls. PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="33836-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="33836-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33836-128">NOTES</span></span>

## <span data-ttu-id="33836-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33836-129">RELATED LINKS</span></span>