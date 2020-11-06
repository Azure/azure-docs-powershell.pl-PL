---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
ms.openlocfilehash: 5a8f82168db41305042e976b9daa1828b2072f95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541807"
---
# <span data-ttu-id="bb30e-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="bb30e-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="bb30e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb30e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb30e-103">Ustawia właściwości rozszerzenia kopii zapasowej na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bb30e-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb30e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb30e-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb30e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bb30e-105">DESCRIPTION</span></span>

## <span data-ttu-id="bb30e-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb30e-106">EXAMPLES</span></span>

### <span data-ttu-id="bb30e-107">1:1</span><span class="sxs-lookup"><span data-stu-id="bb30e-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="bb30e-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb30e-108">PARAMETERS</span></span>

### <span data-ttu-id="bb30e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb30e-109">-DefaultProfile</span></span>
<span data-ttu-id="bb30e-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb30e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb30e-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bb30e-111">-Name</span></span>
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

### <span data-ttu-id="bb30e-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb30e-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="bb30e-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="bb30e-113">-Tag</span></span>
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

### <span data-ttu-id="bb30e-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="bb30e-114">-VMName</span></span>
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

### <span data-ttu-id="bb30e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb30e-115">CommonParameters</span></span>
<span data-ttu-id="bb30e-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb30e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb30e-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb30e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb30e-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb30e-118">INPUTS</span></span>

### <span data-ttu-id="bb30e-119">System. String</span><span class="sxs-lookup"><span data-stu-id="bb30e-119">System.String</span></span>

## <span data-ttu-id="bb30e-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb30e-120">OUTPUTS</span></span>

### <span data-ttu-id="bb30e-121">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bb30e-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bb30e-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb30e-122">NOTES</span></span>

## <span data-ttu-id="bb30e-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb30e-123">RELATED LINKS</span></span>
