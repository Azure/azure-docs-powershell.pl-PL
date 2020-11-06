---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 252a633112c28b1dc1e62a6004e3f67e2b6a343a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549495"
---
# <span data-ttu-id="101ba-101">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="101ba-101">Enable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="101ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="101ba-102">SYNOPSIS</span></span>
<span data-ttu-id="101ba-103">Włącza profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="101ba-103">Enables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="101ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="101ba-104">SYNTAX</span></span>

### <span data-ttu-id="101ba-105">Field</span><span class="sxs-lookup"><span data-stu-id="101ba-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="101ba-106">Stream</span><span class="sxs-lookup"><span data-stu-id="101ba-106">Object</span></span>
```
Enable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="101ba-107">Opis</span><span class="sxs-lookup"><span data-stu-id="101ba-107">DESCRIPTION</span></span>
<span data-ttu-id="101ba-108">Polecenie cmdlet **enable-AzureRmTrafficManagerProfile** włącza profil usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="101ba-108">The **Enable-AzureRmTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="101ba-109">Obiekt profilu można określić za pomocą potoku lub jako wartości parametru.</span><span class="sxs-lookup"><span data-stu-id="101ba-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="101ba-110">Możesz też określić profil przy użyciu parametrów *name* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="101ba-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="101ba-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="101ba-111">EXAMPLES</span></span>

### <span data-ttu-id="101ba-112">Przykład 1: Włączanie profilu określonego za pomocą nazwy</span><span class="sxs-lookup"><span data-stu-id="101ba-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="101ba-113">To polecenie włącza profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="101ba-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="101ba-114">Przykład 2: Włączanie profilu przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="101ba-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerProfile
```

<span data-ttu-id="101ba-115">To polecenie pobiera profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="101ba-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="101ba-116">Następnie polecenie przekazuje ten profil do polecenia cmdlet **enable-AzureRmTrafficManagerProfile** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="101ba-116">The command then passes that profile to the **Enable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="101ba-117">To polecenie cmdlet umożliwia włączenie tego profilu.</span><span class="sxs-lookup"><span data-stu-id="101ba-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="101ba-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="101ba-118">PARAMETERS</span></span>

### <span data-ttu-id="101ba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="101ba-119">-DefaultProfile</span></span>
<span data-ttu-id="101ba-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="101ba-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="101ba-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="101ba-121">-Name</span></span>
<span data-ttu-id="101ba-122">Określa nazwę profilu usługi Traffic Managera, który jest włączany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="101ba-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="101ba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="101ba-123">-ResourceGroupName</span></span>
<span data-ttu-id="101ba-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="101ba-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="101ba-125">To polecenie cmdlet umożliwia profilowi usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="101ba-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="101ba-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="101ba-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="101ba-127">Określa obiekt **TrafficManagerProfile** , który ma zostać włączony.</span><span class="sxs-lookup"><span data-stu-id="101ba-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="101ba-128">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="101ba-128">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="101ba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="101ba-129">CommonParameters</span></span>
<span data-ttu-id="101ba-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="101ba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="101ba-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="101ba-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="101ba-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="101ba-132">INPUTS</span></span>

### <span data-ttu-id="101ba-133">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="101ba-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="101ba-134">To polecenie cmdlet akceptuje obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="101ba-134">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="101ba-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="101ba-135">OUTPUTS</span></span>

### <span data-ttu-id="101ba-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="101ba-136">System.Boolean</span></span>

## <span data-ttu-id="101ba-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="101ba-137">NOTES</span></span>

## <span data-ttu-id="101ba-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="101ba-138">RELATED LINKS</span></span>

[<span data-ttu-id="101ba-139">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="101ba-139">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="101ba-140">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="101ba-140">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="101ba-141">Nowe — AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="101ba-141">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="101ba-142">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="101ba-142">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="101ba-143">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="101ba-143">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


