---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 8d2646c56a8ac659f5beeb6695dc2899fb2f2542
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898946"
---
# <span data-ttu-id="b1672-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b1672-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="b1672-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1672-102">SYNOPSIS</span></span>
<span data-ttu-id="b1672-103">Usuwa rozszerzenie VMAccess z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b1672-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1672-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1672-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1672-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b1672-105">DESCRIPTION</span></span>
<span data-ttu-id="b1672-106">Polecenie cmdlet **Remove-AzureRmVMAccessExtension** usuwa rozszerzenie maszyny wirtualnej dostępu do maszyny wirtualnej (VMAccess) z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b1672-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="b1672-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1672-107">EXAMPLES</span></span>

## <span data-ttu-id="b1672-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1672-108">PARAMETERS</span></span>

### <span data-ttu-id="b1672-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1672-109">-DefaultProfile</span></span>
<span data-ttu-id="b1672-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1672-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1672-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b1672-111">-Force</span></span>
<span data-ttu-id="b1672-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b1672-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1672-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b1672-113">-Name</span></span>
<span data-ttu-id="b1672-114">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1672-114">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1672-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1672-115">-ResourceGroupName</span></span>
<span data-ttu-id="b1672-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b1672-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1672-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="b1672-117">-VMName</span></span>
<span data-ttu-id="b1672-118">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b1672-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="b1672-119">To polecenie cmdlet usuwa VMAccess dla maszyny wirtualnej, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b1672-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1672-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b1672-120">-Confirm</span></span>
<span data-ttu-id="b1672-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1672-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1672-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1672-122">-WhatIf</span></span>
<span data-ttu-id="b1672-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1672-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b1672-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b1672-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1672-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1672-125">CommonParameters</span></span>
<span data-ttu-id="b1672-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1672-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1672-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1672-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1672-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1672-128">INPUTS</span></span>

### <span data-ttu-id="b1672-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b1672-129">None</span></span>
<span data-ttu-id="b1672-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b1672-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1672-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1672-131">OUTPUTS</span></span>

### <span data-ttu-id="b1672-132">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b1672-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b1672-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1672-133">NOTES</span></span>

## <span data-ttu-id="b1672-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1672-134">RELATED LINKS</span></span>

[<span data-ttu-id="b1672-135">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b1672-135">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="b1672-136">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b1672-136">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="b1672-137">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="b1672-137">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
