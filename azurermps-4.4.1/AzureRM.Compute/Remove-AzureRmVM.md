---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
ms.openlocfilehash: 3cc48d103867008b247ce480de43d1ccadc68d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550031"
---
# <span data-ttu-id="a9312-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a9312-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="a9312-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9312-102">SYNOPSIS</span></span>
<span data-ttu-id="a9312-103">Umożliwia usunięcie maszyny wirtualnej z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9312-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9312-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9312-104">SYNTAX</span></span>

### <span data-ttu-id="a9312-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9312-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9312-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a9312-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9312-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a9312-107">DESCRIPTION</span></span>
<span data-ttu-id="a9312-108">Polecenie cmdlet **Remove-AzureRmVM** umożliwia usunięcie maszyny wirtualnej z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9312-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="a9312-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9312-109">EXAMPLES</span></span>

### <span data-ttu-id="a9312-110">Przykład 1: usuwanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a9312-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="a9312-111">To polecenie powoduje usunięcie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9312-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="a9312-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9312-112">PARAMETERS</span></span>

### <span data-ttu-id="a9312-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9312-113">-DefaultProfile</span></span>
<span data-ttu-id="a9312-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9312-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9312-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a9312-115">-Force</span></span>
<span data-ttu-id="a9312-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a9312-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9312-117">-ID</span><span class="sxs-lookup"><span data-stu-id="a9312-117">-Id</span></span>
<span data-ttu-id="a9312-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9312-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9312-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9312-119">-Name</span></span>
<span data-ttu-id="a9312-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a9312-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9312-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9312-121">-ResourceGroupName</span></span>
<span data-ttu-id="a9312-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9312-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9312-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9312-123">-Confirm</span></span>
<span data-ttu-id="a9312-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9312-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9312-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9312-125">-WhatIf</span></span>
<span data-ttu-id="a9312-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9312-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a9312-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9312-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9312-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9312-128">CommonParameters</span></span>
<span data-ttu-id="a9312-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9312-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9312-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9312-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9312-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9312-131">INPUTS</span></span>

## <span data-ttu-id="a9312-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9312-132">OUTPUTS</span></span>

## <span data-ttu-id="a9312-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9312-133">NOTES</span></span>

## <span data-ttu-id="a9312-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9312-134">RELATED LINKS</span></span>

[<span data-ttu-id="a9312-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a9312-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="a9312-136">Nowe — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a9312-136">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="a9312-137">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a9312-137">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="a9312-138">Start — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a9312-138">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="a9312-139">Zatrzymaj — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a9312-139">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="a9312-140">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a9312-140">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


