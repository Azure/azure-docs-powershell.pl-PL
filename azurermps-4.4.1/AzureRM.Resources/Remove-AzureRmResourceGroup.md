---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: 6938cf80f3fa6fb20252e1e4a212133ecd1c62a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549868"
---
# <span data-ttu-id="fb435-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fb435-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="fb435-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb435-102">SYNOPSIS</span></span>
<span data-ttu-id="fb435-103">Usuwa grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb435-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb435-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb435-104">SYNTAX</span></span>

### <span data-ttu-id="fb435-105">Umożliwia wyświetlenie listy grup zasobów na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="fb435-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="fb435-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="fb435-106">(Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb435-107">Umożliwia wyświetlenie listy grup zasobów na podstawie identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="fb435-107">Lists the resource group based in the Id.</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb435-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fb435-108">DESCRIPTION</span></span>
<span data-ttu-id="fb435-109">Polecenie cmdlet **Remove-AzureRmResourceGroup** usuwa grupę zasobów platformy Azure oraz jej zasoby z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fb435-109">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="fb435-110">Aby usunąć zasób, ale pozostawić grupę zasobów, użyj polecenia cmdlet Remove-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="fb435-110">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="fb435-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb435-111">EXAMPLES</span></span>

### <span data-ttu-id="fb435-112">Przykład 1. Usuń grupę zasobów</span><span class="sxs-lookup"><span data-stu-id="fb435-112">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="fb435-113">To polecenie usuwa grupę zasobów ContosoRG01 z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fb435-113">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="fb435-114">Polecenie cmdlet monituje o potwierdzenie i nie zwraca wyników.</span><span class="sxs-lookup"><span data-stu-id="fb435-114">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="fb435-115">Przykład 2: Usuwanie grupy zasobów bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="fb435-115">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="fb435-116">To polecenie używa polecenia cmdlet Get-AzureRmResourceGroup, aby uzyskać ContosoRG01 grupy zasobów, a następnie przekazuje je do polecenia **Remove-AzureRmResourceGroup** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="fb435-116">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="fb435-117">*Pełny* parametr Common jest pobierany na informacje o stanie operacji, a parametr *Force* pomija monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fb435-117">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="fb435-118">Przykład 3: Usuwanie wszystkich grup zasobów</span><span class="sxs-lookup"><span data-stu-id="fb435-118">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="fb435-119">To polecenie używa polecenia cmdlet **Get-AzureRmResourceGroup** w celu uzyskania wszystkich grup zasobów, a następnie przekazuje je do polecenia **Remove-AzureRmResourceGroup** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="fb435-119">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="fb435-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb435-120">PARAMETERS</span></span>

### <span data-ttu-id="fb435-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fb435-121">-ApiVersion</span></span>
<span data-ttu-id="fb435-122">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb435-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="fb435-123">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="fb435-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="fb435-124">-Force</span><span class="sxs-lookup"><span data-stu-id="fb435-124">-Force</span></span>
<span data-ttu-id="fb435-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fb435-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fb435-126">-ID</span><span class="sxs-lookup"><span data-stu-id="fb435-126">-Id</span></span>
<span data-ttu-id="fb435-127">Określa identyfikator grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="fb435-127">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="fb435-128">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="fb435-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb435-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fb435-129">-Name</span></span>
<span data-ttu-id="fb435-130">Określa nazwy grup zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="fb435-130">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="fb435-131">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="fb435-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb435-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="fb435-132">-Pre</span></span>
<span data-ttu-id="fb435-133">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="fb435-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fb435-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fb435-134">-Confirm</span></span>
<span data-ttu-id="fb435-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb435-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb435-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb435-136">-WhatIf</span></span>
<span data-ttu-id="fb435-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb435-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb435-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fb435-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb435-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb435-139">-DefaultProfile</span></span>
<span data-ttu-id="fb435-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb435-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb435-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb435-141">CommonParameters</span></span>
<span data-ttu-id="fb435-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb435-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb435-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb435-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb435-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb435-144">INPUTS</span></span>

### <span data-ttu-id="fb435-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fb435-145">None</span></span>

## <span data-ttu-id="fb435-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb435-146">OUTPUTS</span></span>

### <span data-ttu-id="fb435-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fb435-147">None</span></span>

## <span data-ttu-id="fb435-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb435-148">NOTES</span></span>

## <span data-ttu-id="fb435-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb435-149">RELATED LINKS</span></span>

[<span data-ttu-id="fb435-150">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fb435-150">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="fb435-151">Nowe — AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fb435-151">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="fb435-152">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fb435-152">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


