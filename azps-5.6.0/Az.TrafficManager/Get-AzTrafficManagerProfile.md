---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: 3d843729a9ab51e5a4e1ecf1952f778537e8bf11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987302"
---
# <span data-ttu-id="3bff5-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3bff5-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="3bff5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bff5-102">SYNOPSIS</span></span>
<span data-ttu-id="3bff5-103">Pobiera profil Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="3bff5-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="3bff5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3bff5-104">SYNTAX</span></span>

### <span data-ttu-id="3bff5-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bff5-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bff5-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bff5-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bff5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3bff5-107">DESCRIPTION</span></span>
<span data-ttu-id="3bff5-108">Polecenie **cmdlet Get-AzTrafficManagerProfile** pobiera profil usługi Azure Traffic Manager i zwraca obiekt reprezentujący ten profil.</span><span class="sxs-lookup"><span data-stu-id="3bff5-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="3bff5-109">Określ profil według jego nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3bff5-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="3bff5-110">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany do profilu za pomocą Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bff5-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="3bff5-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3bff5-111">EXAMPLES</span></span>

### <span data-ttu-id="3bff5-112">Przykład 1. Uzyskiwanie profilu</span><span class="sxs-lookup"><span data-stu-id="3bff5-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="3bff5-113">To polecenie pobiera profil o nazwie ContosoProfile w grupie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3bff5-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="3bff5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bff5-114">PARAMETERS</span></span>

### <span data-ttu-id="3bff5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bff5-115">-DefaultProfile</span></span>
<span data-ttu-id="3bff5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3bff5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bff5-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3bff5-117">-Name</span></span>
<span data-ttu-id="3bff5-118">Określa nazwę profilu menedżera ruchu, który będzie pobierał to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bff5-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3bff5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bff5-119">-ResourceGroupName</span></span>
<span data-ttu-id="3bff5-120">Określa nazwę grupy zasobów zawierającej profil menedżera ruchu, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bff5-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3bff5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bff5-121">CommonParameters</span></span>
<span data-ttu-id="3bff5-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bff5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bff5-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bff5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bff5-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bff5-124">INPUTS</span></span>

### <span data-ttu-id="3bff5-125">System.String</span><span class="sxs-lookup"><span data-stu-id="3bff5-125">System.String</span></span>

## <span data-ttu-id="3bff5-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bff5-126">OUTPUTS</span></span>

### <span data-ttu-id="3bff5-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3bff5-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="3bff5-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3bff5-128">NOTES</span></span>

## <span data-ttu-id="3bff5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bff5-129">RELATED LINKS</span></span>

[<span data-ttu-id="3bff5-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3bff5-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="3bff5-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3bff5-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="3bff5-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3bff5-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="3bff5-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3bff5-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="3bff5-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3bff5-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


