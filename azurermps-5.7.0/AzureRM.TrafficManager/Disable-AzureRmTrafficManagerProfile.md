---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 99bff202a67dcc0db6109f3622188e10d250c573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717672"
---
# <span data-ttu-id="bcd6a-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bcd6a-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="bcd6a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bcd6a-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd6a-103">Wyłącza profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcd6a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bcd6a-104">SYNTAX</span></span>

### <span data-ttu-id="bcd6a-105">Field</span><span class="sxs-lookup"><span data-stu-id="bcd6a-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcd6a-106">Stream</span><span class="sxs-lookup"><span data-stu-id="bcd6a-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcd6a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bcd6a-107">DESCRIPTION</span></span>
<span data-ttu-id="bcd6a-108">Polecenie cmdlet **disable-AzureRmTrafficManagerProfile** wyłącza profil usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="bcd6a-109">Obiekt profilu można określić za pomocą potoku lub jako wartości parametru.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="bcd6a-110">Możesz też określić profil przy użyciu parametrów *name* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="bcd6a-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="bcd6a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bcd6a-111">EXAMPLES</span></span>

### <span data-ttu-id="bcd6a-112">Przykład 1. Wyłączanie profilu określonego za pomocą nazwy</span><span class="sxs-lookup"><span data-stu-id="bcd6a-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="bcd6a-113">To polecenie wyłącza profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="bcd6a-114">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="bcd6a-115">Przykład 2: wyłączenie profilu za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="bcd6a-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="bcd6a-116">To polecenie pobiera profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="bcd6a-117">Następnie polecenie przekazuje ten profil do polecenia cmdlet **disable-AzureRmTrafficManagerProfile** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bcd6a-118">To polecenie cmdlet wyłącza ten profil.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="bcd6a-119">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="bcd6a-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="bcd6a-120">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="bcd6a-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bcd6a-121">PARAMETERS</span></span>

### <span data-ttu-id="bcd6a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcd6a-122">-DefaultProfile</span></span>
<span data-ttu-id="bcd6a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcd6a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="bcd6a-124">-Force</span></span>
<span data-ttu-id="bcd6a-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcd6a-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bcd6a-126">-Name</span></span>
<span data-ttu-id="bcd6a-127">Określa nazwę profilu usługi Traffic Managera, który zostanie wyłączony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="bcd6a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcd6a-128">-ResourceGroupName</span></span>
<span data-ttu-id="bcd6a-129">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="bcd6a-130">To polecenie cmdlet wyłącza profil usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bcd6a-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bcd6a-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="bcd6a-132">Określa obiekt **TrafficManagerProfile** , który ma zostać wyłączony.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="bcd6a-133">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="bcd6a-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bcd6a-134">-Confirm</span></span>
<span data-ttu-id="bcd6a-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcd6a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcd6a-136">-WhatIf</span></span>
<span data-ttu-id="bcd6a-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcd6a-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcd6a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd6a-139">CommonParameters</span></span>
<span data-ttu-id="bcd6a-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcd6a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcd6a-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcd6a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd6a-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcd6a-142">INPUTS</span></span>

### <span data-ttu-id="bcd6a-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bcd6a-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="bcd6a-144">To polecenie cmdlet akceptuje obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="bcd6a-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="bcd6a-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bcd6a-145">OUTPUTS</span></span>

### <span data-ttu-id="bcd6a-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bcd6a-146">System.Boolean</span></span>

## <span data-ttu-id="bcd6a-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bcd6a-147">NOTES</span></span>

## <span data-ttu-id="bcd6a-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bcd6a-148">RELATED LINKS</span></span>

[<span data-ttu-id="bcd6a-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bcd6a-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="bcd6a-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bcd6a-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="bcd6a-151">Nowe — AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bcd6a-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="bcd6a-152">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bcd6a-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="bcd6a-153">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bcd6a-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


