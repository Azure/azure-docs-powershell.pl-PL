---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmchefextension
schema: 2.0.0
ms.openlocfilehash: bc8dbd023d8730922614f749f540d182c63237a4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898943"
---
# <span data-ttu-id="98e78-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="98e78-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="98e78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98e78-102">SYNOPSIS</span></span>
<span data-ttu-id="98e78-103">Usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="98e78-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98e78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98e78-104">SYNTAX</span></span>

### <span data-ttu-id="98e78-105">Linux</span><span class="sxs-lookup"><span data-stu-id="98e78-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98e78-106">Microsoft</span><span class="sxs-lookup"><span data-stu-id="98e78-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98e78-107">Opis</span><span class="sxs-lookup"><span data-stu-id="98e78-107">DESCRIPTION</span></span>
<span data-ttu-id="98e78-108">Polecenie cmdlet **Remove-AzureVMChefExtension** usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="98e78-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="98e78-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98e78-109">EXAMPLES</span></span>

### <span data-ttu-id="98e78-110">Przykład 1: Usuwanie rozszerzenia Kuchmistrz z maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="98e78-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="98e78-111">To polecenie usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej opartej na systemie Windows o nazwie WindowsVM001 należącej do grupy zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="98e78-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="98e78-112">Przykład 2: Usuwanie rozszerzenia Kuchmistrz z maszyny wirtualnej Linux</span><span class="sxs-lookup"><span data-stu-id="98e78-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="98e78-113">To polecenie usuwa rozszerzenie Kuchmistrz z maszyny wirtualnej opartej na systemie Linux o nazwie LinuxVM001 należącej do grupy zasobów o nazwie ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="98e78-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="98e78-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98e78-114">PARAMETERS</span></span>

### <span data-ttu-id="98e78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e78-115">-DefaultProfile</span></span>
<span data-ttu-id="98e78-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98e78-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98e78-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="98e78-117">-Linux</span></span>
<span data-ttu-id="98e78-118">Wskazuje, że to polecenie cmdlet ma element docelowy maszyny wirtualnej Linux.</span><span class="sxs-lookup"><span data-stu-id="98e78-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e78-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98e78-119">-Name</span></span>
<span data-ttu-id="98e78-120">Określa nazwę rozszerzenia Kuchmistrz, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98e78-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98e78-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98e78-121">-ResourceGroupName</span></span>
<span data-ttu-id="98e78-122">Określa nazwę grupy zasobów zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="98e78-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="98e78-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="98e78-123">-VMName</span></span>
<span data-ttu-id="98e78-124">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet usuwa rozszerzenie Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="98e78-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="98e78-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="98e78-125">-Windows</span></span>
<span data-ttu-id="98e78-126">Wskazuje, że to polecenie cmdlet ma element docelowy maszyny wirtualnej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="98e78-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e78-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98e78-127">-Confirm</span></span>
<span data-ttu-id="98e78-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98e78-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98e78-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98e78-129">-WhatIf</span></span>
<span data-ttu-id="98e78-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98e78-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="98e78-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="98e78-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98e78-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e78-132">CommonParameters</span></span>
<span data-ttu-id="98e78-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98e78-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98e78-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98e78-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e78-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98e78-135">INPUTS</span></span>

### <span data-ttu-id="98e78-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="98e78-136">None</span></span>
<span data-ttu-id="98e78-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="98e78-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98e78-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98e78-138">OUTPUTS</span></span>

### <span data-ttu-id="98e78-139">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="98e78-139">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="98e78-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98e78-140">NOTES</span></span>

## <span data-ttu-id="98e78-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98e78-141">RELATED LINKS</span></span>

[<span data-ttu-id="98e78-142">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="98e78-142">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="98e78-143">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="98e78-143">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
