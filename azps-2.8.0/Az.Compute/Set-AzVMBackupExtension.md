---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: dfcbc8c9b39faae2212bb26098bcfe0f2a966a3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706196"
---
# <span data-ttu-id="e2a9a-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="e2a9a-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="e2a9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a9a-103">Ustawia właściwości rozszerzenia kopii zapasowej na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e2a9a-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="e2a9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2a9a-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2a9a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e2a9a-105">DESCRIPTION</span></span>

## <span data-ttu-id="e2a9a-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2a9a-106">EXAMPLES</span></span>

### <span data-ttu-id="e2a9a-107">1:1</span><span class="sxs-lookup"><span data-stu-id="e2a9a-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="e2a9a-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2a9a-108">PARAMETERS</span></span>

### <span data-ttu-id="e2a9a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a9a-109">-DefaultProfile</span></span>
<span data-ttu-id="e2a9a-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a9a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2a9a-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2a9a-111">-Name</span></span>
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

### <span data-ttu-id="e2a9a-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2a9a-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e2a9a-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="e2a9a-113">-Tag</span></span>
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

### <span data-ttu-id="e2a9a-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="e2a9a-114">-VMName</span></span>
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

### <span data-ttu-id="e2a9a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a9a-115">CommonParameters</span></span>
<span data-ttu-id="e2a9a-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2a9a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a9a-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2a9a-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a9a-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2a9a-118">INPUTS</span></span>

### <span data-ttu-id="e2a9a-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e2a9a-119">System.String</span></span>

## <span data-ttu-id="e2a9a-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2a9a-120">OUTPUTS</span></span>

### <span data-ttu-id="e2a9a-121">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e2a9a-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e2a9a-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2a9a-122">NOTES</span></span>

## <span data-ttu-id="e2a9a-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2a9a-123">RELATED LINKS</span></span>