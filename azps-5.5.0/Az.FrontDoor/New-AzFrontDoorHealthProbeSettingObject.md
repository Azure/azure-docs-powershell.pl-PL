---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180666"
---
# <span data-ttu-id="8643a-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="8643a-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="8643a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8643a-102">SYNOPSIS</span></span>
<span data-ttu-id="8643a-103">Tworzenie obiektu PSHealthProbeSetting do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="8643a-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="8643a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8643a-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8643a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8643a-105">DESCRIPTION</span></span>
<span data-ttu-id="8643a-106">Tworzenie obiektu PSHealthProbeSetting do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="8643a-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="8643a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8643a-107">EXAMPLES</span></span>

### <span data-ttu-id="8643a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8643a-108">Example 1</span></span>
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

<span data-ttu-id="8643a-109">Uwaga: w ustawieniu HealthProbeMethod nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="8643a-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="8643a-110">Tworzenie obiektu PSHealthProbeSetting do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="8643a-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="8643a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8643a-111">PARAMETERS</span></span>

### <span data-ttu-id="8643a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8643a-112">-DefaultProfile</span></span>
<span data-ttu-id="8643a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8643a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8643a-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="8643a-114">-EnabledState</span></span>
<span data-ttu-id="8643a-115">Czy należy włączyć ochronę kondycji względem zaplecza zdefiniowanych w ramach backendPools.</span><span class="sxs-lookup"><span data-stu-id="8643a-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="8643a-116">Kondycję można wyłączyć tylko wtedy, gdy w jednej włączonej puli zaplecza jest włączona pojedyncza pula zaplecza.</span><span class="sxs-lookup"><span data-stu-id="8643a-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

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

### <span data-ttu-id="8643a-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="8643a-117">-HealthProbeMethod</span></span>
<span data-ttu-id="8643a-118">Konfiguruje metodę HTTP, która ma być stosowana do blokowania zaplecza zdefiniowanego w ramach backendPools.</span><span class="sxs-lookup"><span data-stu-id="8643a-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="8643a-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="8643a-119">-IntervalInSeconds</span></span>
<span data-ttu-id="8643a-120">Liczba sekund między stanem zdrowia.</span><span class="sxs-lookup"><span data-stu-id="8643a-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="8643a-121">Wartość domyślna to 30</span><span class="sxs-lookup"><span data-stu-id="8643a-121">Default value is 30</span></span>

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

### <span data-ttu-id="8643a-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8643a-122">-Name</span></span>
<span data-ttu-id="8643a-123">Nazwa ustawienia kondycji.</span><span class="sxs-lookup"><span data-stu-id="8643a-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="8643a-124">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="8643a-124">-Path</span></span>
<span data-ttu-id="8643a-125">Ścieżka do użycia dla kondycji.</span><span class="sxs-lookup"><span data-stu-id="8643a-125">The path to use for the health probe.</span></span>
<span data-ttu-id="8643a-126">Wartość domyślna to /</span><span class="sxs-lookup"><span data-stu-id="8643a-126">Default is /</span></span>

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

### <span data-ttu-id="8643a-127">— Protokół</span><span class="sxs-lookup"><span data-stu-id="8643a-127">-Protocol</span></span>
<span data-ttu-id="8643a-128">Protocol scheme to use for this probe Default value is HTTP</span><span class="sxs-lookup"><span data-stu-id="8643a-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="8643a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8643a-129">CommonParameters</span></span>
<span data-ttu-id="8643a-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8643a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8643a-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8643a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8643a-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8643a-132">INPUTS</span></span>

### <span data-ttu-id="8643a-133">Brak</span><span class="sxs-lookup"><span data-stu-id="8643a-133">None</span></span>
## <span data-ttu-id="8643a-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8643a-134">OUTPUTS</span></span>

### <span data-ttu-id="8643a-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="8643a-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="8643a-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8643a-136">NOTES</span></span>

## <span data-ttu-id="8643a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8643a-137">RELATED LINKS</span></span>

<span data-ttu-id="8643a-138">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="8643a-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
