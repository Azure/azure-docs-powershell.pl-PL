---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbackupextension
schema: 2.0.0
ms.openlocfilehash: 5d31ad189dcc5337b81373d52a026e01f93f08a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898760"
---
# <span data-ttu-id="3c8da-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="3c8da-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="3c8da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c8da-102">SYNOPSIS</span></span>
<span data-ttu-id="3c8da-103">Ustawia właściwości rozszerzenia kopii zapasowej na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3c8da-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c8da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c8da-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c8da-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3c8da-105">DESCRIPTION</span></span>

## <span data-ttu-id="3c8da-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c8da-106">EXAMPLES</span></span>

### <span data-ttu-id="3c8da-107">1:1</span><span class="sxs-lookup"><span data-stu-id="3c8da-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="3c8da-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c8da-108">PARAMETERS</span></span>

### <span data-ttu-id="3c8da-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c8da-109">-DefaultProfile</span></span>
<span data-ttu-id="3c8da-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c8da-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c8da-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3c8da-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c8da-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c8da-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="3c8da-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="3c8da-113">-Tag</span></span>
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

### <span data-ttu-id="3c8da-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="3c8da-114">-VMName</span></span>
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

### <span data-ttu-id="3c8da-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c8da-115">CommonParameters</span></span>
<span data-ttu-id="3c8da-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c8da-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c8da-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c8da-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c8da-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c8da-118">INPUTS</span></span>

### <span data-ttu-id="3c8da-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3c8da-119">None</span></span>
<span data-ttu-id="3c8da-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3c8da-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3c8da-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c8da-121">OUTPUTS</span></span>

### <span data-ttu-id="3c8da-122">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3c8da-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3c8da-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c8da-123">NOTES</span></span>

## <span data-ttu-id="3c8da-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c8da-124">RELATED LINKS</span></span>

