---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 94a62f9f65be3f859b088d9e0e1d2561d097e7cf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868960"
---
# <span data-ttu-id="d67bf-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="d67bf-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="d67bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d67bf-102">SYNOPSIS</span></span>
<span data-ttu-id="d67bf-103">Usuwa kopię zapasową z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d67bf-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="d67bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d67bf-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d67bf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d67bf-105">DESCRIPTION</span></span>

## <span data-ttu-id="d67bf-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d67bf-106">EXAMPLES</span></span>

### <span data-ttu-id="d67bf-107">1:1</span><span class="sxs-lookup"><span data-stu-id="d67bf-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d67bf-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d67bf-108">PARAMETERS</span></span>

### <span data-ttu-id="d67bf-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67bf-109">-DefaultProfile</span></span>
<span data-ttu-id="d67bf-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d67bf-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d67bf-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d67bf-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d67bf-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="d67bf-112">-Tag</span></span>
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

### <span data-ttu-id="d67bf-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="d67bf-113">-VMName</span></span>
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

### <span data-ttu-id="d67bf-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67bf-114">CommonParameters</span></span>
<span data-ttu-id="d67bf-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d67bf-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d67bf-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d67bf-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67bf-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d67bf-117">INPUTS</span></span>

### <span data-ttu-id="d67bf-118">System. String</span><span class="sxs-lookup"><span data-stu-id="d67bf-118">System.String</span></span>

## <span data-ttu-id="d67bf-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d67bf-119">OUTPUTS</span></span>

### <span data-ttu-id="d67bf-120">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d67bf-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d67bf-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d67bf-121">NOTES</span></span>

## <span data-ttu-id="d67bf-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d67bf-122">RELATED LINKS</span></span>
