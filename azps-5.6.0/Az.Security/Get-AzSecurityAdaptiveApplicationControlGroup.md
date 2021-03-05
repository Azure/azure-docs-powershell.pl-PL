---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: c23c04a5a9df3464bd84a2261435c744374cfb3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011729"
---
# <span data-ttu-id="f2b8a-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="f2b8a-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="f2b8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2b8a-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b8a-103">Pobiera grupę maszyny wirtualnej/serwera kontrolki aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f2b8a-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="f2b8a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f2b8a-104">SYNTAX</span></span>

### <span data-ttu-id="f2b8a-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f2b8a-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2b8a-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="f2b8a-106">DESCRIPTION</span></span>
<span data-ttu-id="f2b8a-107">Adaptacyjne kontrolki aplikacji są automatycznie obliczane przez Azure Security Center. To polecenie cmdlet umożliwia uzyskiwanie grupy sterowanie aplikacją/serwerem.</span><span class="sxs-lookup"><span data-stu-id="f2b8a-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="f2b8a-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f2b8a-108">EXAMPLES</span></span>

### <span data-ttu-id="f2b8a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2b8a-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="f2b8a-110">Pobiera grupę maszyny wirtualnej/serwera kontrolki aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f2b8a-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="f2b8a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2b8a-111">PARAMETERS</span></span>

### <span data-ttu-id="f2b8a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b8a-112">-DefaultProfile</span></span>
<span data-ttu-id="f2b8a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b8a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2b8a-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="f2b8a-114">-AscLocation</span></span>
<span data-ttu-id="f2b8a-115">Lokalizacja, w której centrum asc przechowuje dane subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f2b8a-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="f2b8a-116">można pobrać z lokalizacji Pobierania.</span><span class="sxs-lookup"><span data-stu-id="f2b8a-116">can be retrieved from Get locations.</span></span>

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

### <span data-ttu-id="f2b8a-117">-GroupName</span><span class="sxs-lookup"><span data-stu-id="f2b8a-117">-GroupName</span></span>
<span data-ttu-id="f2b8a-118">Nazwa grupy maszyny wirtualnej/serwera kontrolki aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f2b8a-118">Name of an application control VM/server group.</span></span>

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

### <span data-ttu-id="f2b8a-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2b8a-119">-SubscriptionId</span></span>
<span data-ttu-id="f2b8a-120">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b8a-120">Azure subscription ID.</span></span>

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


### <span data-ttu-id="f2b8a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b8a-121">CommonParameters</span></span>
<span data-ttu-id="f2b8a-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2b8a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b8a-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2b8a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b8a-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2b8a-124">INPUTS</span></span>

### <span data-ttu-id="f2b8a-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f2b8a-125">System.String</span></span>

## <span data-ttu-id="f2b8a-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2b8a-126">OUTPUTS</span></span>

### <span data-ttu-id="f2b8a-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="f2b8a-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="f2b8a-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f2b8a-128">NOTES</span></span>

## <span data-ttu-id="f2b8a-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2b8a-129">RELATED LINKS</span></span>