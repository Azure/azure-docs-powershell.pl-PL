---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501050"
---
# <span data-ttu-id="699dd-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="699dd-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="699dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="699dd-102">SYNOPSIS</span></span>
<span data-ttu-id="699dd-103">Utwórz obiekt PSBackendPoolsSetting do tworzenia przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="699dd-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="699dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="699dd-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="699dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="699dd-105">DESCRIPTION</span></span>
<span data-ttu-id="699dd-106">Polecenie cmdlet **New-AzFrontDoorBackendpoolsSettingObject** tworzy nowy obiekt PSBackendPoolsSettings na potrzeby tworzenia przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="699dd-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="699dd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="699dd-107">EXAMPLES</span></span>

### <span data-ttu-id="699dd-108">Przykład 1: Tworzenie obiektu BackendPoolsSettings przy użyciu domyślnych</span><span class="sxs-lookup"><span data-stu-id="699dd-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="699dd-109">Przykład 2: Tworzenie obiektu BackendPoolsSettings z wartościami określonymi przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="699dd-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="699dd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="699dd-110">PARAMETERS</span></span>

### <span data-ttu-id="699dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699dd-111">-DefaultProfile</span></span>
<span data-ttu-id="699dd-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="699dd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="699dd-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="699dd-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="699dd-114">Czy należy wymusić sprawdzanie nazw certyfikatów na żądania HTTPS we wszystkich pulach zaplecza.</span><span class="sxs-lookup"><span data-stu-id="699dd-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="699dd-115">Brak wpływu na żądania inne niż HTTPS.</span><span class="sxs-lookup"><span data-stu-id="699dd-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="699dd-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="699dd-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="699dd-117">Przekrocz limit czasu wysyłania i odbierania żądań przesyłania dalej w wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="699dd-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="699dd-118">Po osiągnięciu limitu czasu żądanie nie powiedzie się i zwróci wartość.</span><span class="sxs-lookup"><span data-stu-id="699dd-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="699dd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699dd-119">CommonParameters</span></span>
<span data-ttu-id="699dd-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="699dd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699dd-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="699dd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699dd-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="699dd-122">INPUTS</span></span>

### <span data-ttu-id="699dd-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="699dd-123">None</span></span>

## <span data-ttu-id="699dd-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="699dd-124">OUTPUTS</span></span>

### <span data-ttu-id="699dd-125">Microsoft. Azure. Commands. FrontDoor. models. PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="699dd-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="699dd-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="699dd-126">NOTES</span></span>

## <span data-ttu-id="699dd-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="699dd-127">RELATED LINKS</span></span>
