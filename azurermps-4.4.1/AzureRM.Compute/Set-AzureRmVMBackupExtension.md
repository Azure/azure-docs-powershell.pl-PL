---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
ms.openlocfilehash: d95ef152ed21439aafdc1cf9778b101473539b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525586"
---
# <span data-ttu-id="fbfc2-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="fbfc2-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="fbfc2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbfc2-102">SYNOPSIS</span></span>
<span data-ttu-id="fbfc2-103">Ustawia właściwości rozszerzenia kopii zapasowej na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fbfc2-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbfc2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbfc2-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbfc2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fbfc2-105">DESCRIPTION</span></span>

## <span data-ttu-id="fbfc2-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbfc2-106">EXAMPLES</span></span>

### <span data-ttu-id="fbfc2-107">1:1</span><span class="sxs-lookup"><span data-stu-id="fbfc2-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="fbfc2-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbfc2-108">PARAMETERS</span></span>

### <span data-ttu-id="fbfc2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbfc2-109">-DefaultProfile</span></span>
<span data-ttu-id="fbfc2-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbfc2-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbfc2-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fbfc2-111">-Name</span></span>
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

### <span data-ttu-id="fbfc2-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbfc2-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="fbfc2-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="fbfc2-113">-Tag</span></span>
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

### <span data-ttu-id="fbfc2-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="fbfc2-114">-VMName</span></span>
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

### <span data-ttu-id="fbfc2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbfc2-115">CommonParameters</span></span>
<span data-ttu-id="fbfc2-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbfc2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbfc2-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbfc2-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbfc2-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbfc2-118">INPUTS</span></span>

## <span data-ttu-id="fbfc2-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbfc2-119">OUTPUTS</span></span>

## <span data-ttu-id="fbfc2-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbfc2-120">NOTES</span></span>

## <span data-ttu-id="fbfc2-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbfc2-121">RELATED LINKS</span></span>

