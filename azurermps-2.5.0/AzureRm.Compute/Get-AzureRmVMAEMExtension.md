---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: f5936a4be0170279d7416b05dc2b61fd22cfcca5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898057"
---
# <span data-ttu-id="f6eb6-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f6eb6-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="f6eb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="f6eb6-103">Pobiera informacje o rozszerzeniu AEM.</span><span class="sxs-lookup"><span data-stu-id="f6eb6-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6eb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6eb6-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6eb6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f6eb6-105">DESCRIPTION</span></span>
<span data-ttu-id="f6eb6-106">Polecenie cmdlet **Get-AzureRmVMAEMExtension** pobiera informacje o rozszerzeniu usługi Azure enhanceing Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="f6eb6-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="f6eb6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6eb6-107">EXAMPLES</span></span>

### <span data-ttu-id="f6eb6-108">Przykład 1: uzyskiwanie rozszerzenia AEM</span><span class="sxs-lookup"><span data-stu-id="f6eb6-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="f6eb6-109">To polecenie pobiera informacje o rozszerzeniu AEM dla maszyny wirtualnej o nazwie contoso — Server.</span><span class="sxs-lookup"><span data-stu-id="f6eb6-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="f6eb6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6eb6-110">PARAMETERS</span></span>

### <span data-ttu-id="f6eb6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6eb6-111">-DefaultProfile</span></span>
<span data-ttu-id="f6eb6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6eb6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6eb6-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f6eb6-113">-Name</span></span>
<span data-ttu-id="f6eb6-114">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f6eb6-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f6eb6-115">To polecenie cmdlet umożliwia pobieranie informacji dotyczących rozszerzenia AEM na maszynie wirtualnej, którą to polecenie cmdlet określa.</span><span class="sxs-lookup"><span data-stu-id="f6eb6-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="f6eb6-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="f6eb6-116">-OSType</span></span>
<span data-ttu-id="f6eb6-117">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="f6eb6-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="f6eb6-118">Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f6eb6-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="f6eb6-119">Dopuszczalne wartości tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="f6eb6-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6eb6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6eb6-120">-ResourceGroupName</span></span>
<span data-ttu-id="f6eb6-121">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f6eb6-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="f6eb6-122">To polecenie cmdlet umożliwia pobieranie informacji dotyczących rozszerzenia AEM na tej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f6eb6-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="f6eb6-123">-Status</span><span class="sxs-lookup"><span data-stu-id="f6eb6-123">-Status</span></span>
<span data-ttu-id="f6eb6-124">Wskazuje, że to polecenie cmdlet pobiera tylko widok wystąpienia rozszerzenia AEM.</span><span class="sxs-lookup"><span data-stu-id="f6eb6-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6eb6-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="f6eb6-125">-VMName</span></span>
<span data-ttu-id="f6eb6-126">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f6eb6-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f6eb6-127">To polecenie cmdlet umożliwia pobieranie informacji o rozszerzeniu AEM dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="f6eb6-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f6eb6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6eb6-128">CommonParameters</span></span>
<span data-ttu-id="f6eb6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6eb6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6eb6-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6eb6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6eb6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6eb6-131">INPUTS</span></span>

### <span data-ttu-id="f6eb6-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f6eb6-132">None</span></span>
<span data-ttu-id="f6eb6-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f6eb6-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6eb6-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6eb6-134">OUTPUTS</span></span>

### <span data-ttu-id="f6eb6-135">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="f6eb6-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="f6eb6-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6eb6-136">NOTES</span></span>

## <span data-ttu-id="f6eb6-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6eb6-137">RELATED LINKS</span></span>

[<span data-ttu-id="f6eb6-138">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f6eb6-138">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="f6eb6-139">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f6eb6-139">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="f6eb6-140">Test — AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f6eb6-140">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


