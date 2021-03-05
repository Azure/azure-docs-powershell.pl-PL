---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 23ae31c79c33e9299d1cf3dc5998798657408da4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972090"
---
# <span data-ttu-id="0251e-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="0251e-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="0251e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0251e-102">SYNOPSIS</span></span>
<span data-ttu-id="0251e-103">Usuwa kopię zapasową z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0251e-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="0251e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0251e-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0251e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0251e-105">DESCRIPTION</span></span>

## <span data-ttu-id="0251e-106">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0251e-106">EXAMPLES</span></span>

### <span data-ttu-id="0251e-107">1:</span><span class="sxs-lookup"><span data-stu-id="0251e-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="0251e-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0251e-108">PARAMETERS</span></span>

### <span data-ttu-id="0251e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0251e-109">-DefaultProfile</span></span>
<span data-ttu-id="0251e-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0251e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0251e-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0251e-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="0251e-112">— Tag</span><span class="sxs-lookup"><span data-stu-id="0251e-112">-Tag</span></span>
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

### <span data-ttu-id="0251e-113">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="0251e-113">-VMName</span></span>
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

### <span data-ttu-id="0251e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0251e-114">CommonParameters</span></span>
<span data-ttu-id="0251e-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0251e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0251e-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0251e-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0251e-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0251e-117">INPUTS</span></span>

### <span data-ttu-id="0251e-118">System.String</span><span class="sxs-lookup"><span data-stu-id="0251e-118">System.String</span></span>

## <span data-ttu-id="0251e-119">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0251e-119">OUTPUTS</span></span>

### <span data-ttu-id="0251e-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0251e-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0251e-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0251e-121">NOTES</span></span>

## <span data-ttu-id="0251e-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0251e-122">RELATED LINKS</span></span>
