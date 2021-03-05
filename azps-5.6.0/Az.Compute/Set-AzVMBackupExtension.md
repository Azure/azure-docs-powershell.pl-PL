---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 7be9116814af3f11e6bd61668b77df133676ab1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013697"
---
# <span data-ttu-id="2569e-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="2569e-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="2569e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2569e-102">SYNOPSIS</span></span>
<span data-ttu-id="2569e-103">Ustawia właściwości rozszerzenia kopii zapasowej na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="2569e-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="2569e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2569e-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2569e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2569e-105">DESCRIPTION</span></span>

## <span data-ttu-id="2569e-106">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2569e-106">EXAMPLES</span></span>

### <span data-ttu-id="2569e-107">1:</span><span class="sxs-lookup"><span data-stu-id="2569e-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="2569e-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2569e-108">PARAMETERS</span></span>

### <span data-ttu-id="2569e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2569e-109">-DefaultProfile</span></span>
<span data-ttu-id="2569e-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2569e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2569e-111">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2569e-111">-Name</span></span>
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

### <span data-ttu-id="2569e-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2569e-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="2569e-113">— Tag</span><span class="sxs-lookup"><span data-stu-id="2569e-113">-Tag</span></span>
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

### <span data-ttu-id="2569e-114">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="2569e-114">-VMName</span></span>
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

### <span data-ttu-id="2569e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2569e-115">CommonParameters</span></span>
<span data-ttu-id="2569e-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2569e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2569e-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2569e-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2569e-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2569e-118">INPUTS</span></span>

### <span data-ttu-id="2569e-119">System.String</span><span class="sxs-lookup"><span data-stu-id="2569e-119">System.String</span></span>

## <span data-ttu-id="2569e-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2569e-120">OUTPUTS</span></span>

### <span data-ttu-id="2569e-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2569e-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2569e-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2569e-122">NOTES</span></span>

## <span data-ttu-id="2569e-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2569e-123">RELATED LINKS</span></span>
