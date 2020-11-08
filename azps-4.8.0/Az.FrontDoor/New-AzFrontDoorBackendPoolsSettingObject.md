---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221198"
---
# <span data-ttu-id="c3e1d-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="c3e1d-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="c3e1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e1d-103">Utwórz obiekt PSBackendPoolsSetting do tworzenia przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="c3e1d-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="c3e1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3e1d-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3e1d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c3e1d-105">DESCRIPTION</span></span>
<span data-ttu-id="c3e1d-106">Polecenie cmdlet **New-AzFrontDoorBackendpoolsSettingObject** tworzy nowy obiekt PSBackendPoolsSettings na potrzeby tworzenia przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="c3e1d-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="c3e1d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3e1d-107">EXAMPLES</span></span>

### <span data-ttu-id="c3e1d-108">Przykład 1: Tworzenie obiektu BackendPoolsSettings przy użyciu domyślnych</span><span class="sxs-lookup"><span data-stu-id="c3e1d-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="c3e1d-109">Przykład 2: Tworzenie obiektu BackendPoolsSettings z wartościami określonymi przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="c3e1d-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="c3e1d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3e1d-110">PARAMETERS</span></span>

### <span data-ttu-id="c3e1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e1d-111">-DefaultProfile</span></span>
<span data-ttu-id="c3e1d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e1d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3e1d-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="c3e1d-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="c3e1d-114">Czy należy wymusić sprawdzanie nazw certyfikatów na żądania HTTPS we wszystkich pulach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="c3e1d-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="c3e1d-115">Brak wpływu na żądania inne niż HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c3e1d-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="c3e1d-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="c3e1d-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="c3e1d-117">Przekrocz limit czasu wysyłania i odbierania żądań przesyłania dalej w wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="c3e1d-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="c3e1d-118">Po osiągnięciu limitu czasu żądanie nie powiedzie się i zwróci wartość.</span><span class="sxs-lookup"><span data-stu-id="c3e1d-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="c3e1d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e1d-119">CommonParameters</span></span>
<span data-ttu-id="c3e1d-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e1d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e1d-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3e1d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e1d-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3e1d-122">INPUTS</span></span>

### <span data-ttu-id="c3e1d-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c3e1d-123">None</span></span>

## <span data-ttu-id="c3e1d-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3e1d-124">OUTPUTS</span></span>

### <span data-ttu-id="c3e1d-125">Microsoft. Azure. Commands. FrontDoor. models. PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="c3e1d-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="c3e1d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3e1d-126">NOTES</span></span>

## <span data-ttu-id="c3e1d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3e1d-127">RELATED LINKS</span></span>
