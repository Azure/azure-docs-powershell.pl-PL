---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: fc1370da73b9217c5f5f8b24705047f154b50f31
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233744"
---
# <span data-ttu-id="9e1b8-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9e1b8-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="9e1b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e1b8-102">SYNOPSIS</span></span>
<span data-ttu-id="9e1b8-103">Wyłącza profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="9e1b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e1b8-104">SYNTAX</span></span>

### <span data-ttu-id="9e1b8-105">Field</span><span class="sxs-lookup"><span data-stu-id="9e1b8-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e1b8-106">Stream</span><span class="sxs-lookup"><span data-stu-id="9e1b8-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e1b8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9e1b8-107">DESCRIPTION</span></span>
<span data-ttu-id="9e1b8-108">Polecenie cmdlet **disable-AzTrafficManagerProfile** wyłącza profil usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="9e1b8-109">Obiekt profilu można określić za pomocą potoku lub jako wartości parametru.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="9e1b8-110">Możesz też określić profil przy użyciu parametrów *name* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="9e1b8-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="9e1b8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e1b8-111">EXAMPLES</span></span>

### <span data-ttu-id="9e1b8-112">Przykład 1. Wyłączanie profilu określonego za pomocą nazwy</span><span class="sxs-lookup"><span data-stu-id="9e1b8-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="9e1b8-113">To polecenie wyłącza profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="9e1b8-114">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="9e1b8-115">Przykład 2: wyłączenie profilu za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="9e1b8-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="9e1b8-116">To polecenie pobiera profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="9e1b8-117">Następnie polecenie przekazuje ten profil do polecenia cmdlet **disable-AzTrafficManagerProfile** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9e1b8-118">To polecenie cmdlet wyłącza ten profil.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="9e1b8-119">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="9e1b8-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="9e1b8-120">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9e1b8-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e1b8-121">PARAMETERS</span></span>

### <span data-ttu-id="9e1b8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e1b8-122">-DefaultProfile</span></span>
<span data-ttu-id="9e1b8-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e1b8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9e1b8-124">-Force</span></span>
<span data-ttu-id="9e1b8-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e1b8-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9e1b8-126">-Name</span></span>
<span data-ttu-id="9e1b8-127">Określa nazwę profilu usługi Traffic Managera, który zostanie wyłączony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="9e1b8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e1b8-128">-ResourceGroupName</span></span>
<span data-ttu-id="9e1b8-129">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9e1b8-130">To polecenie cmdlet wyłącza profil usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e1b8-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9e1b8-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="9e1b8-132">Określa obiekt **TrafficManagerProfile** , który ma zostać wyłączony.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="9e1b8-133">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="9e1b8-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e1b8-134">-Confirm</span></span>
<span data-ttu-id="9e1b8-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e1b8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e1b8-136">-WhatIf</span></span>
<span data-ttu-id="9e1b8-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e1b8-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e1b8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e1b8-139">CommonParameters</span></span>
<span data-ttu-id="9e1b8-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e1b8-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e1b8-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e1b8-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e1b8-142">INPUTS</span></span>

### <span data-ttu-id="9e1b8-143">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9e1b8-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="9e1b8-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e1b8-144">OUTPUTS</span></span>

### <span data-ttu-id="9e1b8-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e1b8-145">System.Boolean</span></span>

## <span data-ttu-id="9e1b8-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e1b8-146">NOTES</span></span>

## <span data-ttu-id="9e1b8-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e1b8-147">RELATED LINKS</span></span>

[<span data-ttu-id="9e1b8-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9e1b8-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="9e1b8-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9e1b8-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="9e1b8-150">Nowe — AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9e1b8-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="9e1b8-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9e1b8-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="9e1b8-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9e1b8-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


