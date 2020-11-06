---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
ms.openlocfilehash: 164fdd36ca0e97dde33caec1322ddfa2bb6a15c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525646"
---
# <span data-ttu-id="dfb5d-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="dfb5d-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="dfb5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dfb5d-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb5d-103">Usuwa rozszerzenie z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dfb5d-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfb5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dfb5d-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfb5d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dfb5d-105">DESCRIPTION</span></span>
<span data-ttu-id="dfb5d-106">Polecenie cmdlet **Remove-AzureRmVMExtension** usuwa rozszerzenie z rozszerzeń maszyny wirtualnej na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dfb5d-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="dfb5d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dfb5d-107">EXAMPLES</span></span>

### <span data-ttu-id="dfb5d-108">Przykład 1: Usuwanie rozszerzenia z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="dfb5d-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="dfb5d-109">To polecenie usuwa rozszerzenie o nazwie ContosoTest z maszyny wirtualnej o nazwie VirtualMachine22 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="dfb5d-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="dfb5d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dfb5d-110">PARAMETERS</span></span>

### <span data-ttu-id="dfb5d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb5d-111">-DefaultProfile</span></span>
<span data-ttu-id="dfb5d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dfb5d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfb5d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="dfb5d-113">-Force</span></span>
<span data-ttu-id="dfb5d-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dfb5d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dfb5d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dfb5d-115">-Name</span></span>
<span data-ttu-id="dfb5d-116">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfb5d-116">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfb5d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfb5d-117">-ResourceGroupName</span></span>
<span data-ttu-id="dfb5d-118">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dfb5d-118">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfb5d-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="dfb5d-119">-VMName</span></span>
<span data-ttu-id="dfb5d-120">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="dfb5d-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfb5d-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dfb5d-121">-Confirm</span></span>
<span data-ttu-id="dfb5d-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfb5d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfb5d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfb5d-123">-WhatIf</span></span>
<span data-ttu-id="dfb5d-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfb5d-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="dfb5d-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dfb5d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfb5d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb5d-126">CommonParameters</span></span>
<span data-ttu-id="dfb5d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfb5d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb5d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfb5d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb5d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dfb5d-129">INPUTS</span></span>

## <span data-ttu-id="dfb5d-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dfb5d-130">OUTPUTS</span></span>

## <span data-ttu-id="dfb5d-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dfb5d-131">NOTES</span></span>

## <span data-ttu-id="dfb5d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dfb5d-132">RELATED LINKS</span></span>

[<span data-ttu-id="dfb5d-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="dfb5d-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="dfb5d-134">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="dfb5d-134">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


