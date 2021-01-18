---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503533"
---
# <span data-ttu-id="71694-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="71694-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="71694-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71694-102">SYNOPSIS</span></span>
<span data-ttu-id="71694-103">Zwraca klucze funkcji BitLocker dla wszystkich dysków w określonym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="71694-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="71694-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71694-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="71694-105">Opis</span><span class="sxs-lookup"><span data-stu-id="71694-105">DESCRIPTION</span></span>
<span data-ttu-id="71694-106">Zwraca klucze funkcji BitLocker dla wszystkich dysków w określonym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="71694-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="71694-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71694-107">EXAMPLES</span></span>

### <span data-ttu-id="71694-108">Przykład 1: wyświetlanie wszystkich kluczy funkcji BitLocker w określonym zadaniu ImportExport</span><span class="sxs-lookup"><span data-stu-id="71694-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="71694-109">To polecenie cmdlet wyświetla wszystkie klucze funkcji BitLocker określone w określonym zadaniu ImportExport.</span><span class="sxs-lookup"><span data-stu-id="71694-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="71694-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71694-110">PARAMETERS</span></span>

### <span data-ttu-id="71694-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="71694-111">-AcceptLanguage</span></span>
<span data-ttu-id="71694-112">Określa preferowany język odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="71694-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="71694-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71694-113">-DefaultProfile</span></span>
<span data-ttu-id="71694-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71694-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71694-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="71694-115">-JobName</span></span>
<span data-ttu-id="71694-116">Nazwa zadania importu/eksportu.</span><span class="sxs-lookup"><span data-stu-id="71694-116">The name of the import/export job.</span></span>

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

### <span data-ttu-id="71694-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71694-117">-ResourceGroupName</span></span>
<span data-ttu-id="71694-118">Nazwa grupy zasobów jednoznacznie identyfikuje grupę zasobów w ramach abonamentu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="71694-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="71694-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="71694-119">-SubscriptionId</span></span>
<span data-ttu-id="71694-120">Identyfikator subskrypcji użytkownika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="71694-120">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="71694-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71694-121">CommonParameters</span></span>
<span data-ttu-id="71694-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71694-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71694-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71694-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71694-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71694-124">INPUTS</span></span>

## <span data-ttu-id="71694-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71694-125">OUTPUTS</span></span>

### <span data-ttu-id="71694-126">Microsoft. Azure. PowerShell. polecenia. ImportExport. models. Api20161101. IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="71694-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="71694-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71694-127">NOTES</span></span>

<span data-ttu-id="71694-128">PISUJE</span><span class="sxs-lookup"><span data-stu-id="71694-128">ALIASES</span></span>

## <span data-ttu-id="71694-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71694-129">RELATED LINKS</span></span>

