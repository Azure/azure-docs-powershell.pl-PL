---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 85b7a873a921e7fd08055e1e3adc7c70831f8fa1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051079"
---
# <span data-ttu-id="d5d44-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="d5d44-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="d5d44-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5d44-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d44-103">Usuwa kopię zapasową z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d5d44-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="d5d44-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5d44-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5d44-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d5d44-105">DESCRIPTION</span></span>

## <span data-ttu-id="d5d44-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5d44-106">EXAMPLES</span></span>

### <span data-ttu-id="d5d44-107">1:1</span><span class="sxs-lookup"><span data-stu-id="d5d44-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d5d44-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5d44-108">PARAMETERS</span></span>

### <span data-ttu-id="d5d44-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d44-109">-DefaultProfile</span></span>
<span data-ttu-id="d5d44-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d44-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d44-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d44-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d5d44-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="d5d44-112">-Tag</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d44-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="d5d44-113">-VMName</span></span>
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

### <span data-ttu-id="d5d44-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d44-114">CommonParameters</span></span>
<span data-ttu-id="d5d44-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5d44-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d44-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5d44-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d44-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5d44-117">INPUTS</span></span>

### <span data-ttu-id="d5d44-118">System. String</span><span class="sxs-lookup"><span data-stu-id="d5d44-118">System.String</span></span>

## <span data-ttu-id="d5d44-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5d44-119">OUTPUTS</span></span>

### <span data-ttu-id="d5d44-120">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d5d44-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d5d44-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5d44-121">NOTES</span></span>

## <span data-ttu-id="d5d44-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5d44-122">RELATED LINKS</span></span>
