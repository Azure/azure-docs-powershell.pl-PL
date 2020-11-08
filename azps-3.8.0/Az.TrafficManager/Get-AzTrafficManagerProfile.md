---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: c79eb6b5a8883f6b3a9ede2316f47c98fd9b389c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050648"
---
# <span data-ttu-id="c7180-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7180-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="c7180-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7180-102">SYNOPSIS</span></span>
<span data-ttu-id="c7180-103">Pobiera profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="c7180-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="c7180-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7180-104">SYNTAX</span></span>

### <span data-ttu-id="c7180-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7180-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7180-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7180-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7180-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c7180-107">DESCRIPTION</span></span>
<span data-ttu-id="c7180-108">Polecenie cmdlet **Get-AzTrafficManagerProfile** pobiera profil usługi Azure Traffic Manager i zwraca obiekt reprezentujący ten profil.</span><span class="sxs-lookup"><span data-stu-id="c7180-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="c7180-109">Określ profil, podając jego nazwę i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c7180-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="c7180-110">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w profilu przy użyciu polecenia cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="c7180-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="c7180-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7180-111">EXAMPLES</span></span>

### <span data-ttu-id="c7180-112">Przykład 1. Uzyskaj profil</span><span class="sxs-lookup"><span data-stu-id="c7180-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c7180-113">To polecenie pobiera profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c7180-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="c7180-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7180-114">PARAMETERS</span></span>

### <span data-ttu-id="c7180-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7180-115">-DefaultProfile</span></span>
<span data-ttu-id="c7180-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7180-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7180-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c7180-117">-Name</span></span>
<span data-ttu-id="c7180-118">Określa nazwę profilu usługi Traffic Managera, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7180-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7180-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7180-119">-ResourceGroupName</span></span>
<span data-ttu-id="c7180-120">Określa nazwę grupy zasobów zawierającej profil Menedżera ruchu, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7180-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7180-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7180-121">CommonParameters</span></span>
<span data-ttu-id="c7180-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7180-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7180-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7180-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7180-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7180-124">INPUTS</span></span>

### <span data-ttu-id="c7180-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c7180-125">System.String</span></span>

## <span data-ttu-id="c7180-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7180-126">OUTPUTS</span></span>

### <span data-ttu-id="c7180-127">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7180-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="c7180-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7180-128">NOTES</span></span>

## <span data-ttu-id="c7180-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7180-129">RELATED LINKS</span></span>

[<span data-ttu-id="c7180-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7180-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="c7180-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7180-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="c7180-132">Nowe — AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7180-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="c7180-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7180-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="c7180-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7180-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


