---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382907"
---
# <span data-ttu-id="62ad5-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="62ad5-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="62ad5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62ad5-102">SYNOPSIS</span></span>
<span data-ttu-id="62ad5-103">Włącza profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="62ad5-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="62ad5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62ad5-104">SYNTAX</span></span>

### <span data-ttu-id="62ad5-105">Field</span><span class="sxs-lookup"><span data-stu-id="62ad5-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62ad5-106">Stream</span><span class="sxs-lookup"><span data-stu-id="62ad5-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62ad5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="62ad5-107">DESCRIPTION</span></span>
<span data-ttu-id="62ad5-108">Polecenie cmdlet **enable-AzTrafficManagerProfile** włącza profil usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="62ad5-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="62ad5-109">Obiekt profilu można określić za pomocą potoku lub jako wartości parametru.</span><span class="sxs-lookup"><span data-stu-id="62ad5-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="62ad5-110">Możesz też określić profil przy użyciu parametrów *name* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="62ad5-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="62ad5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62ad5-111">EXAMPLES</span></span>

### <span data-ttu-id="62ad5-112">Przykład 1: Włączanie profilu określonego za pomocą nazwy</span><span class="sxs-lookup"><span data-stu-id="62ad5-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="62ad5-113">To polecenie włącza profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="62ad5-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="62ad5-114">Przykład 2: Włączanie profilu przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="62ad5-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="62ad5-115">To polecenie pobiera profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="62ad5-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="62ad5-116">Następnie polecenie przekazuje ten profil do polecenia cmdlet **enable-AzTrafficManagerProfile** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="62ad5-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="62ad5-117">To polecenie cmdlet umożliwia włączenie tego profilu.</span><span class="sxs-lookup"><span data-stu-id="62ad5-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="62ad5-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62ad5-118">PARAMETERS</span></span>

### <span data-ttu-id="62ad5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ad5-119">-DefaultProfile</span></span>
<span data-ttu-id="62ad5-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="62ad5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62ad5-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="62ad5-121">-Name</span></span>
<span data-ttu-id="62ad5-122">Określa nazwę profilu usługi Traffic Managera, który jest włączany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62ad5-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="62ad5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62ad5-123">-ResourceGroupName</span></span>
<span data-ttu-id="62ad5-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="62ad5-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="62ad5-125">To polecenie cmdlet umożliwia profilowi usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="62ad5-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="62ad5-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="62ad5-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="62ad5-127">Określa obiekt **TrafficManagerProfile** , który ma zostać włączony.</span><span class="sxs-lookup"><span data-stu-id="62ad5-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="62ad5-128">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="62ad5-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="62ad5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ad5-129">CommonParameters</span></span>
<span data-ttu-id="62ad5-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62ad5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ad5-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62ad5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ad5-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62ad5-132">INPUTS</span></span>

### <span data-ttu-id="62ad5-133">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="62ad5-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="62ad5-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62ad5-134">OUTPUTS</span></span>

### <span data-ttu-id="62ad5-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62ad5-135">System.Boolean</span></span>

## <span data-ttu-id="62ad5-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62ad5-136">NOTES</span></span>

## <span data-ttu-id="62ad5-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62ad5-137">RELATED LINKS</span></span>

[<span data-ttu-id="62ad5-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="62ad5-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="62ad5-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="62ad5-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="62ad5-140">Nowe — AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="62ad5-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="62ad5-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="62ad5-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="62ad5-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="62ad5-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


