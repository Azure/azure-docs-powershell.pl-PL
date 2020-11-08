---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223910"
---
# <span data-ttu-id="686f3-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="686f3-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="686f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="686f3-102">SYNOPSIS</span></span>
<span data-ttu-id="686f3-103">Tworzenie obiektu PSHealthProbeSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="686f3-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="686f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="686f3-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="686f3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="686f3-105">DESCRIPTION</span></span>
<span data-ttu-id="686f3-106">Tworzenie obiektu PSHealthProbeSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="686f3-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="686f3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="686f3-107">EXAMPLES</span></span>

### <span data-ttu-id="686f3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="686f3-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
HealthProbeMethod : Head
EnabledState      : Enabled
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="686f3-109">Uwaga: w ustawieniach HealthProbeMethod nie jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="686f3-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="686f3-110">Tworzenie obiektu PSHealthProbeSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="686f3-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="686f3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="686f3-111">PARAMETERS</span></span>

### <span data-ttu-id="686f3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="686f3-112">-DefaultProfile</span></span>
<span data-ttu-id="686f3-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="686f3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="686f3-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="686f3-114">-EnabledState</span></span>
<span data-ttu-id="686f3-115">Określa, czy włączyć badania kondycji na koniec z innymi w obszarze backendPools.</span><span class="sxs-lookup"><span data-stu-id="686f3-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="686f3-116">Badania kondycji można wyłączyć tylko w przypadku włączenia jednej wewnętrznej bazy danych w ramach jednej z włączonych puli zaplecza.</span><span class="sxs-lookup"><span data-stu-id="686f3-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

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

### <span data-ttu-id="686f3-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="686f3-117">-HealthProbeMethod</span></span>
<span data-ttu-id="686f3-118">Określa metodę HTTP, która ma być używana do sondowania zakończeń zdefiniowanych w obszarze backendPools.</span><span class="sxs-lookup"><span data-stu-id="686f3-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="686f3-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="686f3-119">-IntervalInSeconds</span></span>
<span data-ttu-id="686f3-120">Liczba sekund między badaniami kondycji.</span><span class="sxs-lookup"><span data-stu-id="686f3-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="686f3-121">Wartość domyślna to 30</span><span class="sxs-lookup"><span data-stu-id="686f3-121">Default value is 30</span></span>

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

### <span data-ttu-id="686f3-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="686f3-122">-Name</span></span>
<span data-ttu-id="686f3-123">Nazwa ustawienia badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="686f3-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="686f3-124">-Path</span><span class="sxs-lookup"><span data-stu-id="686f3-124">-Path</span></span>
<span data-ttu-id="686f3-125">Ścieżka używana do badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="686f3-125">The path to use for the health probe.</span></span>
<span data-ttu-id="686f3-126">Wartość domyślna to/</span><span class="sxs-lookup"><span data-stu-id="686f3-126">Default is /</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="686f3-127">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="686f3-127">-Protocol</span></span>
<span data-ttu-id="686f3-128">Schemat protokołu do użycia w przypadku tej sondy wartość domyślna to HTTP</span><span class="sxs-lookup"><span data-stu-id="686f3-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="686f3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="686f3-129">CommonParameters</span></span>
<span data-ttu-id="686f3-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="686f3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="686f3-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="686f3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="686f3-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="686f3-132">INPUTS</span></span>

### <span data-ttu-id="686f3-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="686f3-133">None</span></span>
## <span data-ttu-id="686f3-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="686f3-134">OUTPUTS</span></span>

### <span data-ttu-id="686f3-135">Microsoft. Azure. Commands. FrontDoor. models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="686f3-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="686f3-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="686f3-136">NOTES</span></span>

## <span data-ttu-id="686f3-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="686f3-137">RELATED LINKS</span></span>

<span data-ttu-id="686f3-138">[Nowe — AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="686f3-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
