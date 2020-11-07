---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: ce07d1a46fe0f13b18238d9e20fb1d4b28b7d861
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893401"
---
# <span data-ttu-id="c0ca3-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="c0ca3-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="c0ca3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ca3-103">Ustawia właściwości rozszerzenia kopii zapasowej na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c0ca3-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="c0ca3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0ca3-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0ca3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c0ca3-105">DESCRIPTION</span></span>

## <span data-ttu-id="c0ca3-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0ca3-106">EXAMPLES</span></span>

### <span data-ttu-id="c0ca3-107">1:1</span><span class="sxs-lookup"><span data-stu-id="c0ca3-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="c0ca3-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0ca3-108">PARAMETERS</span></span>

### <span data-ttu-id="c0ca3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ca3-109">-DefaultProfile</span></span>
<span data-ttu-id="c0ca3-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0ca3-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0ca3-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c0ca3-111">-Name</span></span>
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

### <span data-ttu-id="c0ca3-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0ca3-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c0ca3-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="c0ca3-113">-Tag</span></span>
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

### <span data-ttu-id="c0ca3-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="c0ca3-114">-VMName</span></span>
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

### <span data-ttu-id="c0ca3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ca3-115">CommonParameters</span></span>
<span data-ttu-id="c0ca3-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0ca3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ca3-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0ca3-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ca3-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0ca3-118">INPUTS</span></span>

### <span data-ttu-id="c0ca3-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c0ca3-119">None</span></span>
<span data-ttu-id="c0ca3-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c0ca3-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c0ca3-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0ca3-121">OUTPUTS</span></span>

### <span data-ttu-id="c0ca3-122">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c0ca3-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c0ca3-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0ca3-123">NOTES</span></span>

## <span data-ttu-id="c0ca3-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0ca3-124">RELATED LINKS</span></span>

