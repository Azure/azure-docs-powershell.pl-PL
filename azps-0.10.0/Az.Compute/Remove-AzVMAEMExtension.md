---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 224d11aba6eece63c7c080415253b4833c665cee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893570"
---
# <span data-ttu-id="9576b-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9576b-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="9576b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9576b-102">SYNOPSIS</span></span>
<span data-ttu-id="9576b-103">Usuwa rozszerzenie AEM z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9576b-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="9576b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9576b-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9576b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9576b-105">DESCRIPTION</span></span>
<span data-ttu-id="9576b-106">Polecenie cmdlet **Remove-AzVMAEMExtension** usuwa rozszerzenie rozszerzonego monitorowania platformy Azure (AEM) z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9576b-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="9576b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9576b-107">EXAMPLES</span></span>

### <span data-ttu-id="9576b-108">Przykład 1. Usuń rozszerzenie AEM</span><span class="sxs-lookup"><span data-stu-id="9576b-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="9576b-109">To polecenie usuwa rozszerzenie AEM dla maszyny wirtualnej o nazwie contoso — serwer.</span><span class="sxs-lookup"><span data-stu-id="9576b-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="9576b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9576b-110">PARAMETERS</span></span>

### <span data-ttu-id="9576b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9576b-111">-DefaultProfile</span></span>
<span data-ttu-id="9576b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9576b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9576b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9576b-113">-Name</span></span>
<span data-ttu-id="9576b-114">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie AEM.</span><span class="sxs-lookup"><span data-stu-id="9576b-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="9576b-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="9576b-115">-OSType</span></span>
<span data-ttu-id="9576b-116">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="9576b-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="9576b-117">Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9576b-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="9576b-118">Dopuszczalne wartości tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="9576b-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9576b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9576b-119">-ResourceGroupName</span></span>
<span data-ttu-id="9576b-120">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9576b-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="9576b-121">To polecenie cmdlet usuwa rozszerzenie AEM z tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9576b-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="9576b-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="9576b-122">-VMName</span></span>
<span data-ttu-id="9576b-123">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9576b-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9576b-124">To polecenie cmdlet usuwa rozszerzenie AEM dla maszyny wirtualnej, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9576b-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="9576b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9576b-125">CommonParameters</span></span>
<span data-ttu-id="9576b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9576b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9576b-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9576b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9576b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9576b-128">INPUTS</span></span>

### <span data-ttu-id="9576b-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9576b-129">None</span></span>
<span data-ttu-id="9576b-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9576b-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9576b-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9576b-131">OUTPUTS</span></span>

### <span data-ttu-id="9576b-132">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9576b-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9576b-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9576b-133">NOTES</span></span>

## <span data-ttu-id="9576b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9576b-134">RELATED LINKS</span></span>

[<span data-ttu-id="9576b-135">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9576b-135">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="9576b-136">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9576b-136">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="9576b-137">Test — AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9576b-137">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


