---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 459ede802e3a96805bb2c32e4e901592604f03b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544031"
---
# <span data-ttu-id="b0237-101">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b0237-101">Remove-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="b0237-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0237-102">SYNOPSIS</span></span>
<span data-ttu-id="b0237-103">Usuwa profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="b0237-103">Deletes a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0237-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0237-104">SYNTAX</span></span>

### <span data-ttu-id="b0237-105">Field</span><span class="sxs-lookup"><span data-stu-id="b0237-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0237-106">Stream</span><span class="sxs-lookup"><span data-stu-id="b0237-106">Object</span></span>
```
Remove-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0237-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b0237-107">DESCRIPTION</span></span>
<span data-ttu-id="b0237-108">Polecenie cmdlet **Remove-AzureRmTrafficManagerProfile** usuwa profil usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="b0237-108">The **Remove-AzureRmTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="b0237-109">Określ profil, który chcesz usunąć, przy użyciu parametrów *name* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="b0237-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="b0237-110">Można też określić obiekt **TrafficManagerProfile** za pomocą parametru *TrafficManagerProfile* lub za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="b0237-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="b0237-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0237-111">EXAMPLES</span></span>

### <span data-ttu-id="b0237-112">Przykład 1: Usuwanie profilu określonego za pomocą nazwy</span><span class="sxs-lookup"><span data-stu-id="b0237-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="b0237-113">To polecenie usuwa profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b0237-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="b0237-114">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b0237-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="b0237-115">Przykład 2: Usuwanie profilu za pomocą rurociągu</span><span class="sxs-lookup"><span data-stu-id="b0237-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="b0237-116">To polecenie pobiera profil o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b0237-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="b0237-117">Następnie polecenie przekazuje ten profil do polecenia cmdlet **Remove-AzureRmTrafficManagerProfile** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="b0237-117">The command then passes that profile to the **Remove-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b0237-118">Polecenie cmdlet powoduje usunięcie tego profilu.</span><span class="sxs-lookup"><span data-stu-id="b0237-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="b0237-119">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="b0237-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b0237-120">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b0237-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b0237-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0237-121">PARAMETERS</span></span>

### <span data-ttu-id="b0237-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0237-122">-DefaultProfile</span></span>
<span data-ttu-id="b0237-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0237-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0237-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b0237-124">-Force</span></span>
<span data-ttu-id="b0237-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b0237-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b0237-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b0237-126">-Name</span></span>
<span data-ttu-id="b0237-127">Określa nazwę profilu usługi Traffic Managera, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0237-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="b0237-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0237-128">-ResourceGroupName</span></span>
<span data-ttu-id="b0237-129">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0237-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b0237-130">To polecenie cmdlet usuwa profil usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="b0237-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b0237-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b0237-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="b0237-132">Określa obiekt **TrafficManagerProfile** do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b0237-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="b0237-133">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b0237-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="b0237-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b0237-134">-Confirm</span></span>
<span data-ttu-id="b0237-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0237-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0237-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0237-136">-WhatIf</span></span>
<span data-ttu-id="b0237-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0237-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0237-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b0237-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0237-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0237-139">CommonParameters</span></span>
<span data-ttu-id="b0237-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0237-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0237-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0237-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0237-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0237-142">INPUTS</span></span>

### <span data-ttu-id="b0237-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b0237-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="b0237-144">To polecenie cmdlet akceptuje obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="b0237-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="b0237-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0237-145">OUTPUTS</span></span>

### <span data-ttu-id="b0237-146">Wartość</span><span class="sxs-lookup"><span data-stu-id="b0237-146">Boolean</span></span>
<span data-ttu-id="b0237-147">To polecenie cmdlet zwraca wartość $True, jeśli ta operacja się powiedzie lub, Jeśli usunięcie nie powiedzie się, wartość $False.</span><span class="sxs-lookup"><span data-stu-id="b0237-147">This cmdlet returns a value of $True, if it succeeds or, if the deletion fails, a value of $False.</span></span>

## <span data-ttu-id="b0237-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0237-148">NOTES</span></span>

## <span data-ttu-id="b0237-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0237-149">RELATED LINKS</span></span>

[<span data-ttu-id="b0237-150">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b0237-150">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b0237-151">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b0237-151">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b0237-152">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b0237-152">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b0237-153">Nowe — AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b0237-153">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b0237-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b0237-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


