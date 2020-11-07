---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmbackup
schema: 2.0.0
ms.openlocfilehash: 8805d5da061ef19037768b72c08145e45c8f2a9c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898944"
---
# <span data-ttu-id="98a63-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="98a63-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="98a63-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98a63-102">SYNOPSIS</span></span>
<span data-ttu-id="98a63-103">Usuwa kopię zapasową z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="98a63-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98a63-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98a63-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98a63-105">Opis</span><span class="sxs-lookup"><span data-stu-id="98a63-105">DESCRIPTION</span></span>

## <span data-ttu-id="98a63-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98a63-106">EXAMPLES</span></span>

### <span data-ttu-id="98a63-107">1:1</span><span class="sxs-lookup"><span data-stu-id="98a63-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="98a63-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98a63-108">PARAMETERS</span></span>

### <span data-ttu-id="98a63-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a63-109">-DefaultProfile</span></span>
<span data-ttu-id="98a63-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98a63-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98a63-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98a63-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="98a63-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="98a63-112">-Tag</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98a63-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="98a63-113">-VMName</span></span>
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

### <span data-ttu-id="98a63-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a63-114">CommonParameters</span></span>
<span data-ttu-id="98a63-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98a63-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a63-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98a63-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a63-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98a63-117">INPUTS</span></span>

### <span data-ttu-id="98a63-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="98a63-118">None</span></span>
<span data-ttu-id="98a63-119">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="98a63-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98a63-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98a63-120">OUTPUTS</span></span>

### <span data-ttu-id="98a63-121">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="98a63-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="98a63-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98a63-122">NOTES</span></span>

## <span data-ttu-id="98a63-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98a63-123">RELATED LINKS</span></span>

