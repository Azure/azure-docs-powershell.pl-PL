---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: 96f9a3195747aff8d31261b7a6ae992a00adb82b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526249"
---
# <span data-ttu-id="9c64a-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9c64a-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="9c64a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c64a-102">SYNOPSIS</span></span>
<span data-ttu-id="9c64a-103">Usuwa rozszerzenie AEM z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c64a-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c64a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c64a-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c64a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9c64a-105">DESCRIPTION</span></span>
<span data-ttu-id="9c64a-106">Polecenie cmdlet **Remove-AzureRmVMAEMExtension** usuwa rozszerzenie rozszerzonego monitorowania platformy Azure (AEM) z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c64a-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="9c64a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c64a-107">EXAMPLES</span></span>

### <span data-ttu-id="9c64a-108">Przykład 1. Usuń rozszerzenie AEM</span><span class="sxs-lookup"><span data-stu-id="9c64a-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="9c64a-109">To polecenie usuwa rozszerzenie AEM dla maszyny wirtualnej o nazwie contoso — serwer.</span><span class="sxs-lookup"><span data-stu-id="9c64a-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="9c64a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c64a-110">PARAMETERS</span></span>

### <span data-ttu-id="9c64a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c64a-111">-DefaultProfile</span></span>
<span data-ttu-id="9c64a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c64a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c64a-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9c64a-113">-Name</span></span>
<span data-ttu-id="9c64a-114">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie AEM.</span><span class="sxs-lookup"><span data-stu-id="9c64a-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c64a-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="9c64a-115">-OSType</span></span>
<span data-ttu-id="9c64a-116">Określa typ systemu operacyjnego dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="9c64a-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="9c64a-117">Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9c64a-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="9c64a-118">Dopuszczalne wartości tego parametru to: Windows i Linux.</span><span class="sxs-lookup"><span data-stu-id="9c64a-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c64a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c64a-119">-ResourceGroupName</span></span>
<span data-ttu-id="9c64a-120">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c64a-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="9c64a-121">To polecenie cmdlet usuwa rozszerzenie AEM z tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c64a-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="9c64a-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="9c64a-122">-VMName</span></span>
<span data-ttu-id="9c64a-123">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c64a-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9c64a-124">To polecenie cmdlet usuwa rozszerzenie AEM dla maszyny wirtualnej, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9c64a-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="9c64a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c64a-125">CommonParameters</span></span>
<span data-ttu-id="9c64a-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c64a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c64a-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c64a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c64a-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c64a-128">INPUTS</span></span>

### <span data-ttu-id="9c64a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9c64a-129">System.String</span></span>

## <span data-ttu-id="9c64a-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c64a-130">OUTPUTS</span></span>

### <span data-ttu-id="9c64a-131">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9c64a-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9c64a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c64a-132">NOTES</span></span>

## <span data-ttu-id="9c64a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c64a-133">RELATED LINKS</span></span>

[<span data-ttu-id="9c64a-134">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9c64a-134">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="9c64a-135">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9c64a-135">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="9c64a-136">Test — AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9c64a-136">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


