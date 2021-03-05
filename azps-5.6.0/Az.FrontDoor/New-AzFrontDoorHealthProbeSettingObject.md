---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 4d65985d724033244f761748634adb3b2002a199
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971018"
---
# <span data-ttu-id="76381-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="76381-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="76381-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76381-102">SYNOPSIS</span></span>
<span data-ttu-id="76381-103">Tworzenie obiektu PSHealthProbeSetting do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="76381-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="76381-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="76381-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76381-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="76381-105">DESCRIPTION</span></span>
<span data-ttu-id="76381-106">Tworzenie obiektu PSHealthProbeSetting do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="76381-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="76381-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="76381-107">EXAMPLES</span></span>

### <span data-ttu-id="76381-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76381-108">Example 1</span></span>
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

<span data-ttu-id="76381-109">Uwaga: w ustawieniu HealthProbeMethod nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="76381-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="76381-110">Tworzenie obiektu PSHealthProbeSetting do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="76381-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="76381-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76381-111">PARAMETERS</span></span>

### <span data-ttu-id="76381-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76381-112">-DefaultProfile</span></span>
<span data-ttu-id="76381-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="76381-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76381-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="76381-114">-EnabledState</span></span>
<span data-ttu-id="76381-115">Czy należy włączyć ochronę kondycji względem zaplecza zdefiniowanych w ramach backendPools.</span><span class="sxs-lookup"><span data-stu-id="76381-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="76381-116">Kondycję można wyłączyć tylko wtedy, gdy w jednej włączonej puli zaplecza jest włączona pojedyncza pula zaplecza.</span><span class="sxs-lookup"><span data-stu-id="76381-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

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

### <span data-ttu-id="76381-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="76381-117">-HealthProbeMethod</span></span>
<span data-ttu-id="76381-118">Konfiguruje metodę HTTP używaną do uwierzytelniania zaplecza zdefiniowanych w ramach backendPools.</span><span class="sxs-lookup"><span data-stu-id="76381-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="76381-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="76381-119">-IntervalInSeconds</span></span>
<span data-ttu-id="76381-120">Liczba sekund między stanem zdrowia.</span><span class="sxs-lookup"><span data-stu-id="76381-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="76381-121">Wartość domyślna to 30</span><span class="sxs-lookup"><span data-stu-id="76381-121">Default value is 30</span></span>

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

### <span data-ttu-id="76381-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="76381-122">-Name</span></span>
<span data-ttu-id="76381-123">Nazwa ustawienia kondycji.</span><span class="sxs-lookup"><span data-stu-id="76381-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="76381-124">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="76381-124">-Path</span></span>
<span data-ttu-id="76381-125">Ścieżka do użycia dla kondycji.</span><span class="sxs-lookup"><span data-stu-id="76381-125">The path to use for the health probe.</span></span>
<span data-ttu-id="76381-126">Wartość domyślna to /</span><span class="sxs-lookup"><span data-stu-id="76381-126">Default is /</span></span>

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

### <span data-ttu-id="76381-127">— Protokół</span><span class="sxs-lookup"><span data-stu-id="76381-127">-Protocol</span></span>
<span data-ttu-id="76381-128">Protocol scheme to use for this probe Default value is HTTP</span><span class="sxs-lookup"><span data-stu-id="76381-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="76381-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76381-129">CommonParameters</span></span>
<span data-ttu-id="76381-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76381-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76381-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76381-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76381-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76381-132">INPUTS</span></span>

### <span data-ttu-id="76381-133">Brak</span><span class="sxs-lookup"><span data-stu-id="76381-133">None</span></span>
## <span data-ttu-id="76381-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76381-134">OUTPUTS</span></span>

### <span data-ttu-id="76381-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="76381-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="76381-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="76381-136">NOTES</span></span>

## <span data-ttu-id="76381-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76381-137">RELATED LINKS</span></span>

<span data-ttu-id="76381-138">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="76381-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
