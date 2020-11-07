---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 60eaa3b5482d6d1c13236560f797383d68d97b44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705389"
---
# <span data-ttu-id="6fd0d-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="6fd0d-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="6fd0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6fd0d-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd0d-103">Tworzenie obiektu PSHealthProbeSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="6fd0d-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="6fd0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6fd0d-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fd0d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6fd0d-105">DESCRIPTION</span></span>
<span data-ttu-id="6fd0d-106">Tworzenie obiektu PSHealthProbeSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="6fd0d-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="6fd0d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6fd0d-107">EXAMPLES</span></span>

### <span data-ttu-id="6fd0d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6fd0d-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="6fd0d-109">Tworzenie obiektu PSHealthProbeSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="6fd0d-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="6fd0d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fd0d-110">PARAMETERS</span></span>

### <span data-ttu-id="6fd0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd0d-111">-DefaultProfile</span></span>
<span data-ttu-id="6fd0d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd0d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fd0d-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="6fd0d-113">-IntervalInSeconds</span></span>
<span data-ttu-id="6fd0d-114">Liczba sekund między badaniami kondycji.</span><span class="sxs-lookup"><span data-stu-id="6fd0d-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="6fd0d-115">Wartość domyślna to 30</span><span class="sxs-lookup"><span data-stu-id="6fd0d-115">Default value is 30</span></span>

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

### <span data-ttu-id="6fd0d-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6fd0d-116">-Name</span></span>
<span data-ttu-id="6fd0d-117">Nazwa ustawienia badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="6fd0d-117">health probe setting name.</span></span>

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

### <span data-ttu-id="6fd0d-118">-Path</span><span class="sxs-lookup"><span data-stu-id="6fd0d-118">-Path</span></span>
<span data-ttu-id="6fd0d-119">Ścieżka używana do badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="6fd0d-119">The path to use for the health probe.</span></span>
<span data-ttu-id="6fd0d-120">Wartość domyślna to/</span><span class="sxs-lookup"><span data-stu-id="6fd0d-120">Default is /</span></span>

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

### <span data-ttu-id="6fd0d-121">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="6fd0d-121">-Protocol</span></span>
<span data-ttu-id="6fd0d-122">Schemat protokołu do użycia w przypadku tej sondy wartość domyślna to HTTP</span><span class="sxs-lookup"><span data-stu-id="6fd0d-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="6fd0d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd0d-123">CommonParameters</span></span>
<span data-ttu-id="6fd0d-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd0d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd0d-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fd0d-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd0d-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fd0d-126">INPUTS</span></span>

### <span data-ttu-id="6fd0d-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6fd0d-127">None</span></span>

## <span data-ttu-id="6fd0d-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6fd0d-128">OUTPUTS</span></span>

### <span data-ttu-id="6fd0d-129">Microsoft. Azure. Commands. FrontDoor. models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="6fd0d-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="6fd0d-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6fd0d-130">NOTES</span></span>

## <span data-ttu-id="6fd0d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fd0d-131">RELATED LINKS</span></span>

<span data-ttu-id="6fd0d-132">[Nowe — AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="6fd0d-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
