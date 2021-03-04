---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: 4d667b1435a7396082f0626d8f55882f7c37b8ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950810"
---
# <span data-ttu-id="8e89d-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8e89d-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="8e89d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e89d-102">SYNOPSIS</span></span>
<span data-ttu-id="8e89d-103">Wyłącza profil Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="8e89d-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="8e89d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8e89d-104">SYNTAX</span></span>

### <span data-ttu-id="8e89d-105">Pola</span><span class="sxs-lookup"><span data-stu-id="8e89d-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e89d-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="8e89d-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e89d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8e89d-107">DESCRIPTION</span></span>
<span data-ttu-id="8e89d-108">Polecenie **cmdlet Disable-AzTrafficManagerProfile** wyłącza profil usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="8e89d-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="8e89d-109">Obiekt profilu można określić przy użyciu potoku lub wartości parametru.</span><span class="sxs-lookup"><span data-stu-id="8e89d-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="8e89d-110">Możesz również określić profil, używając parametrów *Name (Nazwa)* i *ResourceGroupName (Nazwa* grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="8e89d-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="8e89d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8e89d-111">EXAMPLES</span></span>

### <span data-ttu-id="8e89d-112">Przykład 1. Wyłączanie profilu określonego przez nazwę</span><span class="sxs-lookup"><span data-stu-id="8e89d-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="8e89d-113">To polecenie wyłącza profil o nazwie ContosoProfile w grupie Zasobów11.</span><span class="sxs-lookup"><span data-stu-id="8e89d-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="8e89d-114">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8e89d-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="8e89d-115">Przykład 2. Wyłączanie profilu przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="8e89d-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="8e89d-116">To polecenie pobiera profil o nazwie ContosoProfile w grupie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8e89d-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="8e89d-117">Następnie polecenie przekazuje ten profil do polecenia cmdlet **Disable-AzTrafficManagerProfile** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="8e89d-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8e89d-118">To polecenie cmdlet wyłącza ten profil.</span><span class="sxs-lookup"><span data-stu-id="8e89d-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="8e89d-119">Polecenie określa parametr *Force.*</span><span class="sxs-lookup"><span data-stu-id="8e89d-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8e89d-120">Dlatego nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8e89d-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8e89d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e89d-121">PARAMETERS</span></span>

### <span data-ttu-id="8e89d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e89d-122">-DefaultProfile</span></span>
<span data-ttu-id="8e89d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e89d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e89d-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="8e89d-124">-Force</span></span>
<span data-ttu-id="8e89d-125">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8e89d-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8e89d-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8e89d-126">-Name</span></span>
<span data-ttu-id="8e89d-127">Określa nazwę profilu menedżera ruchu, który zostanie wyłączany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e89d-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="8e89d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e89d-128">-ResourceGroupName</span></span>
<span data-ttu-id="8e89d-129">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8e89d-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8e89d-130">To polecenie cmdlet wyłącza profil menedżera ruchu w grupie, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="8e89d-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e89d-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8e89d-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="8e89d-132">Określa obiekt **TrafficManagerProfile** do wyłączenia.</span><span class="sxs-lookup"><span data-stu-id="8e89d-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="8e89d-133">Aby uzyskać obiekt **TrafficManagerProfile,** użyj Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e89d-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="8e89d-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e89d-134">-Confirm</span></span>
<span data-ttu-id="8e89d-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8e89d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e89d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e89d-136">-WhatIf</span></span>
<span data-ttu-id="8e89d-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e89d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e89d-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8e89d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e89d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e89d-139">CommonParameters</span></span>
<span data-ttu-id="8e89d-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e89d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e89d-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e89d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e89d-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e89d-142">INPUTS</span></span>

### <span data-ttu-id="8e89d-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8e89d-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="8e89d-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e89d-144">OUTPUTS</span></span>

### <span data-ttu-id="8e89d-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8e89d-145">System.Boolean</span></span>

## <span data-ttu-id="8e89d-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8e89d-146">NOTES</span></span>

## <span data-ttu-id="8e89d-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e89d-147">RELATED LINKS</span></span>

[<span data-ttu-id="8e89d-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8e89d-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="8e89d-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8e89d-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="8e89d-150">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8e89d-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="8e89d-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8e89d-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="8e89d-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8e89d-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


