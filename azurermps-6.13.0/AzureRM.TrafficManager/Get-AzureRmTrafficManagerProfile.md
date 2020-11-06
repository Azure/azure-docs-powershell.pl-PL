---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 239e0147b1955c59dbe34591f85273f05aa12c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525938"
---
# <span data-ttu-id="fb7dd-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb7dd-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="fb7dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb7dd-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7dd-103">Pobiera profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="fb7dd-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb7dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb7dd-104">SYNTAX</span></span>

### <span data-ttu-id="fb7dd-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb7dd-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb7dd-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb7dd-106">AccountNameParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb7dd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fb7dd-107">DESCRIPTION</span></span>
<span data-ttu-id="fb7dd-108">Polecenie cmdlet **Get-AzureRmTrafficManagerProfile** pobiera profil usługi Azure Traffic Manager i zwraca obiekt reprezentujący ten profil.</span><span class="sxs-lookup"><span data-stu-id="fb7dd-108">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="fb7dd-109">Określ profil, podając jego nazwę i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb7dd-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="fb7dd-110">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w profilu przy użyciu polecenia cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="fb7dd-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="fb7dd-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb7dd-111">EXAMPLES</span></span>

### <span data-ttu-id="fb7dd-112">Przykład 1. Uzyskaj profil</span><span class="sxs-lookup"><span data-stu-id="fb7dd-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="fb7dd-113">To polecenie pobiera profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fb7dd-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="fb7dd-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb7dd-114">PARAMETERS</span></span>

### <span data-ttu-id="fb7dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7dd-115">-DefaultProfile</span></span>
<span data-ttu-id="fb7dd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb7dd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb7dd-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fb7dd-117">-Name</span></span>
<span data-ttu-id="fb7dd-118">Określa nazwę profilu usługi Traffic Managera, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb7dd-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fb7dd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb7dd-119">-ResourceGroupName</span></span>
<span data-ttu-id="fb7dd-120">Określa nazwę grupy zasobów zawierającej profil Menedżera ruchu, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb7dd-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fb7dd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7dd-121">CommonParameters</span></span>
<span data-ttu-id="fb7dd-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb7dd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7dd-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb7dd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7dd-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb7dd-124">INPUTS</span></span>

### <span data-ttu-id="fb7dd-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fb7dd-125">None</span></span>
<span data-ttu-id="fb7dd-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="fb7dd-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb7dd-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb7dd-127">OUTPUTS</span></span>

### <span data-ttu-id="fb7dd-128">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb7dd-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="fb7dd-129">To polecenie cmdlet zwraca obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="fb7dd-129">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="fb7dd-130">Możesz zmodyfikować ten obiekt, a następnie zastosować zmiany w usłudze Traffic Manager przy użyciu polecenia **Set-AzureRmTrafficManagerProfile**.</span><span class="sxs-lookup"><span data-stu-id="fb7dd-130">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="fb7dd-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb7dd-131">NOTES</span></span>

## <span data-ttu-id="fb7dd-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb7dd-132">RELATED LINKS</span></span>

[<span data-ttu-id="fb7dd-133">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb7dd-133">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fb7dd-134">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb7dd-134">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fb7dd-135">Nowe — AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb7dd-135">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fb7dd-136">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb7dd-136">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fb7dd-137">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fb7dd-137">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


