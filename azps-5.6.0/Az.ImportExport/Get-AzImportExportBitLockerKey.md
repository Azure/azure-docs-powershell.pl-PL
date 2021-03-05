---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: fefd529b00b88c20b3703e1bcecbbb88c72d52e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963002"
---
# <span data-ttu-id="2cca5-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="2cca5-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="2cca5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cca5-102">SYNOPSIS</span></span>
<span data-ttu-id="2cca5-103">Zwraca klucze funkcji BitLocker dla wszystkich dysków w określonym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="2cca5-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="2cca5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2cca5-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2cca5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2cca5-105">DESCRIPTION</span></span>
<span data-ttu-id="2cca5-106">Zwraca klucze funkcji BitLocker dla wszystkich dysków w określonym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="2cca5-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="2cca5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2cca5-107">EXAMPLES</span></span>

### <span data-ttu-id="2cca5-108">Przykład 1. Lista wszystkich kluczy funkcji BitLocker w określonym zadaniu ImportExport</span><span class="sxs-lookup"><span data-stu-id="2cca5-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="2cca5-109">To polecenie cmdlet wyświetla listę wszystkich kluczy funkcji BitLocker w określonym zadaniu ImportExport.</span><span class="sxs-lookup"><span data-stu-id="2cca5-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="2cca5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cca5-110">PARAMETERS</span></span>

### <span data-ttu-id="2cca5-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="2cca5-111">-AcceptLanguage</span></span>
<span data-ttu-id="2cca5-112">Określa preferowany język odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="2cca5-112">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cca5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cca5-113">-DefaultProfile</span></span>
<span data-ttu-id="2cca5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2cca5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cca5-115">— JobName</span><span class="sxs-lookup"><span data-stu-id="2cca5-115">-JobName</span></span>
<span data-ttu-id="2cca5-116">Nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="2cca5-116">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cca5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cca5-117">-ResourceGroupName</span></span>
<span data-ttu-id="2cca5-118">Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2cca5-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cca5-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2cca5-119">-SubscriptionId</span></span>
<span data-ttu-id="2cca5-120">Identyfikator subskrypcji dla użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2cca5-120">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cca5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cca5-121">CommonParameters</span></span>
<span data-ttu-id="2cca5-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cca5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cca5-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cca5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cca5-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2cca5-124">INPUTS</span></span>

## <span data-ttu-id="2cca5-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2cca5-125">OUTPUTS</span></span>

### <span data-ttu-id="2cca5-126">Microsoft.Azure.PowerShell.cmdlet.ImportExport.Models.Api20161101.IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="2cca5-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="2cca5-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2cca5-127">NOTES</span></span>

<span data-ttu-id="2cca5-128">ALIASY</span><span class="sxs-lookup"><span data-stu-id="2cca5-128">ALIASES</span></span>

## <span data-ttu-id="2cca5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2cca5-129">RELATED LINKS</span></span>

