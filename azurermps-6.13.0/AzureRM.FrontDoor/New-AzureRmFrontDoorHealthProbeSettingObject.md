---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: dcaf61b9001093d25f351d03e8e50da4c4ca22ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545332"
---
# <span data-ttu-id="9c677-101">New-AzureRmFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="9c677-101">New-AzureRmFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="9c677-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c677-102">SYNOPSIS</span></span>
<span data-ttu-id="9c677-103">Tworzenie obiektu PSHealthProbeSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="9c677-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c677-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c677-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c677-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9c677-105">DESCRIPTION</span></span>
<span data-ttu-id="9c677-106">Tworzenie obiektu PSHealthProbeSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="9c677-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="9c677-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c677-107">EXAMPLES</span></span>

### <span data-ttu-id="9c677-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9c677-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="9c677-109">Tworzenie obiektu PSHealthProbeSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="9c677-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="9c677-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c677-110">PARAMETERS</span></span>

### <span data-ttu-id="9c677-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c677-111">-DefaultProfile</span></span>
<span data-ttu-id="9c677-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c677-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c677-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9c677-113">-IntervalInSeconds</span></span>
<span data-ttu-id="9c677-114">Liczba sekund między badaniami kondycji.</span><span class="sxs-lookup"><span data-stu-id="9c677-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="9c677-115">Wartość domyślna to 30</span><span class="sxs-lookup"><span data-stu-id="9c677-115">Default value is 30</span></span>

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

### <span data-ttu-id="9c677-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9c677-116">-Name</span></span>
<span data-ttu-id="9c677-117">Nazwa ustawienia badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="9c677-117">health probe setting name.</span></span>

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

### <span data-ttu-id="9c677-118">-Path</span><span class="sxs-lookup"><span data-stu-id="9c677-118">-Path</span></span>
<span data-ttu-id="9c677-119">Ścieżka używana do badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="9c677-119">The path to use for the health probe.</span></span>
<span data-ttu-id="9c677-120">Wartość domyślna to/</span><span class="sxs-lookup"><span data-stu-id="9c677-120">Default is /</span></span>

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

### <span data-ttu-id="9c677-121">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="9c677-121">-Protocol</span></span>
<span data-ttu-id="9c677-122">Schemat protokołu do użycia w przypadku tej sondy wartość domyślna to HTTP</span><span class="sxs-lookup"><span data-stu-id="9c677-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="9c677-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c677-123">CommonParameters</span></span>
<span data-ttu-id="9c677-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c677-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c677-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c677-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c677-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c677-126">INPUTS</span></span>

### <span data-ttu-id="9c677-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9c677-127">None</span></span>

## <span data-ttu-id="9c677-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c677-128">OUTPUTS</span></span>

### <span data-ttu-id="9c677-129">Microsoft. Azure. Commands. FrontDoor. models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="9c677-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="9c677-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c677-130">NOTES</span></span>

## <span data-ttu-id="9c677-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c677-131">RELATED LINKS</span></span>

<span data-ttu-id="9c677-132">[Nowe — AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="9c677-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
