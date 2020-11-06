---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bdfe37622db49c554f128714ab2af65a11fbfce7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549496"
---
# <span data-ttu-id="e1900-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e1900-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="e1900-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1900-102">SYNOPSIS</span></span>
<span data-ttu-id="e1900-103">Pobiera profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="e1900-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1900-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1900-104">SYNTAX</span></span>

```
Get-AzureRmTrafficManagerProfile [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1900-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e1900-105">DESCRIPTION</span></span>
<span data-ttu-id="e1900-106">Polecenie cmdlet **Get-AzureRmTrafficManagerProfile** pobiera profil usługi Azure Traffic Manager i zwraca obiekt reprezentujący ten profil.</span><span class="sxs-lookup"><span data-stu-id="e1900-106">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="e1900-107">Określ profil, podając jego nazwę i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e1900-107">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="e1900-108">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w profilu przy użyciu polecenia cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e1900-108">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="e1900-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1900-109">EXAMPLES</span></span>

### <span data-ttu-id="e1900-110">Przykład 1. Uzyskaj profil</span><span class="sxs-lookup"><span data-stu-id="e1900-110">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="e1900-111">To polecenie pobiera profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e1900-111">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="e1900-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1900-112">PARAMETERS</span></span>

### <span data-ttu-id="e1900-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1900-113">-DefaultProfile</span></span>
<span data-ttu-id="e1900-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1900-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1900-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e1900-115">-Name</span></span>
<span data-ttu-id="e1900-116">Określa nazwę profilu usługi Traffic Managera, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1900-116">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1900-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1900-117">-ResourceGroupName</span></span>
<span data-ttu-id="e1900-118">Określa nazwę grupy zasobów zawierającej profil Menedżera ruchu, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1900-118">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1900-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1900-119">CommonParameters</span></span>
<span data-ttu-id="e1900-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1900-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1900-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1900-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1900-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1900-122">INPUTS</span></span>

### <span data-ttu-id="e1900-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e1900-123">None</span></span>
<span data-ttu-id="e1900-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e1900-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1900-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1900-125">OUTPUTS</span></span>

### <span data-ttu-id="e1900-126">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e1900-126">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="e1900-127">To polecenie cmdlet zwraca obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="e1900-127">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="e1900-128">Możesz zmodyfikować ten obiekt, a następnie zastosować zmiany w usłudze Traffic Manager przy użyciu polecenia **Set-AzureRmTrafficManagerProfile**.</span><span class="sxs-lookup"><span data-stu-id="e1900-128">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="e1900-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1900-129">NOTES</span></span>

## <span data-ttu-id="e1900-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1900-130">RELATED LINKS</span></span>

[<span data-ttu-id="e1900-131">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e1900-131">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="e1900-132">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e1900-132">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="e1900-133">Nowe — AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e1900-133">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="e1900-134">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e1900-134">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="e1900-135">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e1900-135">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


