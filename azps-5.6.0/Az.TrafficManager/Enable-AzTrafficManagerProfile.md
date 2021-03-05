---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: 40bfe0d68df65b7535ec40a3cb27da1501f915c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987337"
---
# <span data-ttu-id="b2666-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2666-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="b2666-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2666-102">SYNOPSIS</span></span>
<span data-ttu-id="b2666-103">Włącza profil Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="b2666-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="b2666-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b2666-104">SYNTAX</span></span>

### <span data-ttu-id="b2666-105">Pola</span><span class="sxs-lookup"><span data-stu-id="b2666-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2666-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="b2666-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2666-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b2666-107">DESCRIPTION</span></span>
<span data-ttu-id="b2666-108">Polecenie **cmdlet Enable-AzTrafficManagerProfile** umożliwia włączenie profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="b2666-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="b2666-109">Obiekt profilu można określić przy użyciu potoku lub wartości parametru.</span><span class="sxs-lookup"><span data-stu-id="b2666-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="b2666-110">Możesz również określić profil, używając parametrów *Name (Nazwa)* i *ResourceGroupName (Nazwa* grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="b2666-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="b2666-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b2666-111">EXAMPLES</span></span>

### <span data-ttu-id="b2666-112">Przykład 1. Włączanie profilu określonego przez nazwę</span><span class="sxs-lookup"><span data-stu-id="b2666-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="b2666-113">To polecenie włącza profil o nazwie ContosoProfile w grupie Zasobów11.</span><span class="sxs-lookup"><span data-stu-id="b2666-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="b2666-114">Przykład 2. Włączanie profilu przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="b2666-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="b2666-115">To polecenie pobiera profil o nazwie ContosoProfile w grupie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b2666-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="b2666-116">Następnie polecenie przekazuje ten profil do polecenia cmdlet **Enable-AzTrafficManagerProfile** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="b2666-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b2666-117">To polecenie cmdlet włącza ten profil.</span><span class="sxs-lookup"><span data-stu-id="b2666-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="b2666-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2666-118">PARAMETERS</span></span>

### <span data-ttu-id="b2666-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2666-119">-DefaultProfile</span></span>
<span data-ttu-id="b2666-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2666-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2666-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b2666-121">-Name</span></span>
<span data-ttu-id="b2666-122">Określa nazwę profilu Menedżera ruchu włączaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2666-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2666-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2666-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2666-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2666-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b2666-125">To polecenie cmdlet włącza profil menedżera ruchu w grupie, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b2666-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2666-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2666-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="b2666-127">Określa obiekt **TrafficManagerProfile** do włączenia.</span><span class="sxs-lookup"><span data-stu-id="b2666-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="b2666-128">Aby uzyskać obiekt **TrafficManagerProfile,** użyj Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2666-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2666-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2666-129">CommonParameters</span></span>
<span data-ttu-id="b2666-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2666-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2666-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2666-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2666-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2666-132">INPUTS</span></span>

### <span data-ttu-id="b2666-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2666-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b2666-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2666-134">OUTPUTS</span></span>

### <span data-ttu-id="b2666-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b2666-135">System.Boolean</span></span>

## <span data-ttu-id="b2666-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b2666-136">NOTES</span></span>

## <span data-ttu-id="b2666-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2666-137">RELATED LINKS</span></span>

[<span data-ttu-id="b2666-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2666-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="b2666-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2666-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="b2666-140">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2666-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="b2666-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2666-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="b2666-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2666-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


