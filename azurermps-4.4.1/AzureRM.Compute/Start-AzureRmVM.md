---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
ms.openlocfilehash: 3091cb877ff792527cf97e3d44b7c363f9dd94b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527706"
---
# <span data-ttu-id="ccab8-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccab8-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="ccab8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ccab8-102">SYNOPSIS</span></span>
<span data-ttu-id="ccab8-103">Rozpoczynanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ccab8-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccab8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ccab8-104">SYNTAX</span></span>

### <span data-ttu-id="ccab8-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ccab8-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccab8-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ccab8-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ccab8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ccab8-107">DESCRIPTION</span></span>
<span data-ttu-id="ccab8-108">Polecenie cmdlet **Start-AzureRmVM** rozpoczyna działanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ccab8-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="ccab8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ccab8-109">EXAMPLES</span></span>

### <span data-ttu-id="ccab8-110">Przykład 1. uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ccab8-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="ccab8-111">To polecenie umożliwia uruchomienie maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ccab8-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="ccab8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ccab8-112">PARAMETERS</span></span>

### <span data-ttu-id="ccab8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccab8-113">-DefaultProfile</span></span>
<span data-ttu-id="ccab8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ccab8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccab8-115">-ID</span><span class="sxs-lookup"><span data-stu-id="ccab8-115">-Id</span></span>
<span data-ttu-id="ccab8-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ccab8-116">The resource group name.</span></span>

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

### <span data-ttu-id="ccab8-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ccab8-117">-Name</span></span>
<span data-ttu-id="ccab8-118">Nazwa maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ccab8-118">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccab8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccab8-119">-ResourceGroupName</span></span>
<span data-ttu-id="ccab8-120">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ccab8-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ccab8-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ccab8-121">-Confirm</span></span>
<span data-ttu-id="ccab8-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccab8-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccab8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccab8-123">-WhatIf</span></span>
<span data-ttu-id="ccab8-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccab8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccab8-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ccab8-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccab8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccab8-126">CommonParameters</span></span>
<span data-ttu-id="ccab8-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccab8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccab8-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccab8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccab8-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ccab8-129">INPUTS</span></span>

## <span data-ttu-id="ccab8-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ccab8-130">OUTPUTS</span></span>

## <span data-ttu-id="ccab8-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ccab8-131">NOTES</span></span>

## <span data-ttu-id="ccab8-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ccab8-132">RELATED LINKS</span></span>

[<span data-ttu-id="ccab8-133">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccab8-133">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ccab8-134">Nowe — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccab8-134">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="ccab8-135">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccab8-135">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="ccab8-136">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccab8-136">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="ccab8-137">Zatrzymaj — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccab8-137">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="ccab8-138">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccab8-138">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


