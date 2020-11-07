---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 02040fcb80fbf020b9d9dd3725369e75fbbf15c8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893550"
---
# <span data-ttu-id="2e9dc-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="2e9dc-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="2e9dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="2e9dc-103">Usuwa kopię zapasową z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2e9dc-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="2e9dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e9dc-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e9dc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e9dc-105">DESCRIPTION</span></span>

## <span data-ttu-id="2e9dc-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e9dc-106">EXAMPLES</span></span>

### <span data-ttu-id="2e9dc-107">1:1</span><span class="sxs-lookup"><span data-stu-id="2e9dc-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="2e9dc-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e9dc-108">PARAMETERS</span></span>

### <span data-ttu-id="2e9dc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e9dc-109">-DefaultProfile</span></span>
<span data-ttu-id="2e9dc-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e9dc-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e9dc-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e9dc-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="2e9dc-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e9dc-112">-Tag</span></span>
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

### <span data-ttu-id="2e9dc-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="2e9dc-113">-VMName</span></span>
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

### <span data-ttu-id="2e9dc-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e9dc-114">CommonParameters</span></span>
<span data-ttu-id="2e9dc-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e9dc-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e9dc-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e9dc-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e9dc-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e9dc-117">INPUTS</span></span>

### <span data-ttu-id="2e9dc-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2e9dc-118">None</span></span>
<span data-ttu-id="2e9dc-119">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="2e9dc-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e9dc-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e9dc-120">OUTPUTS</span></span>

### <span data-ttu-id="2e9dc-121">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2e9dc-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2e9dc-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e9dc-122">NOTES</span></span>

## <span data-ttu-id="2e9dc-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e9dc-123">RELATED LINKS</span></span>

