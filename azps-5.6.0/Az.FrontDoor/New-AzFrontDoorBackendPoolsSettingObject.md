---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: c61c39bc95ae3521d7b0b573c43e303749999cbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971089"
---
# <span data-ttu-id="ae220-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="ae220-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="ae220-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae220-102">SYNOPSIS</span></span>
<span data-ttu-id="ae220-103">Utwórz obiekt PSBackendPoolsSetting do utworzenia drzwi frontowych.</span><span class="sxs-lookup"><span data-stu-id="ae220-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="ae220-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae220-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae220-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae220-105">DESCRIPTION</span></span>
<span data-ttu-id="ae220-106">Polecenie **cmdlet New-AzFrontDoorBackendpoolsSettingObject** tworzy nowy obiekt PSBackendPoolsSettings do tworzenia drzwi frontowych.</span><span class="sxs-lookup"><span data-stu-id="ae220-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="ae220-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae220-107">EXAMPLES</span></span>

### <span data-ttu-id="ae220-108">Przykład 1. Tworzenie obiektu BackendPoolsSettings przy użyciu wartości domyślnych</span><span class="sxs-lookup"><span data-stu-id="ae220-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="ae220-109">Przykład 2. Tworzenie obiektu BackendPoolsSettings przy użyciu wartości określonych przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="ae220-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="ae220-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae220-110">PARAMETERS</span></span>

### <span data-ttu-id="ae220-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae220-111">-DefaultProfile</span></span>
<span data-ttu-id="ae220-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae220-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae220-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="ae220-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="ae220-114">Wymuszanie sprawdzania nazwy certyfikatu we żądaniach HTTPS we wszystkich pulach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="ae220-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="ae220-115">Brak wpływu na żądania inne niż HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ae220-115">No effect on non-HTTPS requests.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae220-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="ae220-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="ae220-117">Wysyłanie i odbieranie limitu czasu dla żądania przesyłania dalej do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="ae220-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="ae220-118">Po osiągnięciu limitu czasu żądanie kończy się niepowodzeniem i zwraca.</span><span class="sxs-lookup"><span data-stu-id="ae220-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="ae220-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae220-119">CommonParameters</span></span>
<span data-ttu-id="ae220-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae220-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae220-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae220-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae220-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae220-122">INPUTS</span></span>

### <span data-ttu-id="ae220-123">Brak</span><span class="sxs-lookup"><span data-stu-id="ae220-123">None</span></span>

## <span data-ttu-id="ae220-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae220-124">OUTPUTS</span></span>

### <span data-ttu-id="ae220-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="ae220-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="ae220-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae220-126">NOTES</span></span>

## <span data-ttu-id="ae220-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae220-127">RELATED LINKS</span></span>
