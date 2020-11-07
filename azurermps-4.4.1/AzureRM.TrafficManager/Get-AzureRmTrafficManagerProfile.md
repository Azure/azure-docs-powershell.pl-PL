---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 6be04cea9e3e73a06cdbb1ee449adaefd4fe803e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719220"
---
# <span data-ttu-id="0419b-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0419b-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="0419b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0419b-102">SYNOPSIS</span></span>
<span data-ttu-id="0419b-103">Pobiera profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="0419b-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0419b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0419b-104">SYNTAX</span></span>

```
Get-AzureRmTrafficManagerProfile [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0419b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0419b-105">DESCRIPTION</span></span>
<span data-ttu-id="0419b-106">Polecenie cmdlet **Get-AzureRmTrafficManagerProfile** pobiera profil usługi Azure Traffic Manager i zwraca obiekt reprezentujący ten profil.</span><span class="sxs-lookup"><span data-stu-id="0419b-106">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="0419b-107">Określ profil, podając jego nazwę i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0419b-107">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="0419b-108">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w profilu przy użyciu polecenia cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0419b-108">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="0419b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0419b-109">EXAMPLES</span></span>

### <span data-ttu-id="0419b-110">Przykład 1. Uzyskaj profil</span><span class="sxs-lookup"><span data-stu-id="0419b-110">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="0419b-111">To polecenie pobiera profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0419b-111">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="0419b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0419b-112">PARAMETERS</span></span>

### <span data-ttu-id="0419b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0419b-113">-Name</span></span>
<span data-ttu-id="0419b-114">Określa nazwę profilu usługi Traffic Managera, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0419b-114">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0419b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0419b-115">-ResourceGroupName</span></span>
<span data-ttu-id="0419b-116">Określa nazwę grupy zasobów zawierającej profil Menedżera ruchu, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0419b-116">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0419b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0419b-117">-DefaultProfile</span></span>
<span data-ttu-id="0419b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0419b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0419b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0419b-119">CommonParameters</span></span>
<span data-ttu-id="0419b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0419b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0419b-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0419b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0419b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0419b-122">INPUTS</span></span>

## <span data-ttu-id="0419b-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0419b-123">OUTPUTS</span></span>

### <span data-ttu-id="0419b-124">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0419b-124">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="0419b-125">To polecenie cmdlet zwraca obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="0419b-125">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="0419b-126">Możesz zmodyfikować ten obiekt, a następnie zastosować zmiany w usłudze Traffic Manager przy użyciu polecenia **Set-AzureRmTrafficManagerProfile**.</span><span class="sxs-lookup"><span data-stu-id="0419b-126">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="0419b-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0419b-127">NOTES</span></span>

## <span data-ttu-id="0419b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0419b-128">RELATED LINKS</span></span>

[<span data-ttu-id="0419b-129">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0419b-129">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0419b-130">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0419b-130">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0419b-131">Nowe — AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0419b-131">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0419b-132">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0419b-132">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0419b-133">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0419b-133">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


