---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 640aed5ccfb38a2dca6989048e3185774ceda15a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232910"
---
# <span data-ttu-id="3af28-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3af28-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="3af28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3af28-102">SYNOPSIS</span></span>
<span data-ttu-id="3af28-103">Usuwa profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="3af28-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="3af28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3af28-104">SYNTAX</span></span>

### <span data-ttu-id="3af28-105">Field</span><span class="sxs-lookup"><span data-stu-id="3af28-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3af28-106">Stream</span><span class="sxs-lookup"><span data-stu-id="3af28-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3af28-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3af28-107">DESCRIPTION</span></span>
<span data-ttu-id="3af28-108">Polecenie cmdlet **Remove-AzTrafficManagerProfile** usuwa profil usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="3af28-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="3af28-109">Określ profil, który chcesz usunąć, przy użyciu parametrów *name* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="3af28-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="3af28-110">Można też określić obiekt **TrafficManagerProfile** za pomocą parametru *TrafficManagerProfile* lub za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="3af28-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="3af28-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3af28-111">EXAMPLES</span></span>

### <span data-ttu-id="3af28-112">Przykład 1: Usuwanie profilu określonego za pomocą nazwy</span><span class="sxs-lookup"><span data-stu-id="3af28-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="3af28-113">To polecenie usuwa profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3af28-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="3af28-114">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3af28-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="3af28-115">Przykład 2: Usuwanie profilu za pomocą rurociągu</span><span class="sxs-lookup"><span data-stu-id="3af28-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="3af28-116">To polecenie pobiera profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3af28-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="3af28-117">Następnie polecenie przekazuje ten profil do polecenia cmdlet **Remove-AzTrafficManagerProfile** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="3af28-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3af28-118">Polecenie cmdlet powoduje usunięcie tego profilu.</span><span class="sxs-lookup"><span data-stu-id="3af28-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="3af28-119">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="3af28-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="3af28-120">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3af28-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3af28-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3af28-121">PARAMETERS</span></span>

### <span data-ttu-id="3af28-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af28-122">-DefaultProfile</span></span>
<span data-ttu-id="3af28-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3af28-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3af28-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3af28-124">-Force</span></span>
<span data-ttu-id="3af28-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3af28-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3af28-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3af28-126">-Name</span></span>
<span data-ttu-id="3af28-127">Określa nazwę profilu usługi Traffic Managera, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3af28-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="3af28-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af28-128">-ResourceGroupName</span></span>
<span data-ttu-id="3af28-129">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3af28-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3af28-130">To polecenie cmdlet usuwa profil usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="3af28-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3af28-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3af28-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="3af28-132">Określa obiekt **TrafficManagerProfile** do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="3af28-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="3af28-133">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="3af28-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="3af28-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3af28-134">-Confirm</span></span>
<span data-ttu-id="3af28-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3af28-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3af28-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3af28-136">-WhatIf</span></span>
<span data-ttu-id="3af28-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3af28-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3af28-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3af28-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3af28-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af28-139">CommonParameters</span></span>
<span data-ttu-id="3af28-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3af28-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af28-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3af28-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af28-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3af28-142">INPUTS</span></span>

### <span data-ttu-id="3af28-143">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3af28-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="3af28-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3af28-144">OUTPUTS</span></span>

### <span data-ttu-id="3af28-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3af28-145">System.Boolean</span></span>

## <span data-ttu-id="3af28-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3af28-146">NOTES</span></span>

## <span data-ttu-id="3af28-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3af28-147">RELATED LINKS</span></span>

[<span data-ttu-id="3af28-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3af28-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="3af28-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3af28-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="3af28-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3af28-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="3af28-151">Nowe — AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3af28-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="3af28-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3af28-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


