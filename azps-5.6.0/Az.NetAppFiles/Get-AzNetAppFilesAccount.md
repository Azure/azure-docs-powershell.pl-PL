---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 9741a150dd26e3fef513984fa4ae8b6a2e7c97b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968657"
---
# <span data-ttu-id="c645b-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c645b-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="c645b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c645b-102">SYNOPSIS</span></span>
<span data-ttu-id="c645b-103">Pobiera szczegółowe informacje o koncie usługi Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="c645b-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="c645b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c645b-104">SYNTAX</span></span>

### <span data-ttu-id="c645b-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c645b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c645b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c645b-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c645b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c645b-107">DESCRIPTION</span></span>
<span data-ttu-id="c645b-108">Polecenie **cmdlet Get-AzNetAppFilesAccount** pobiera szczegółowe informacje o koncie ANF.</span><span class="sxs-lookup"><span data-stu-id="c645b-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="c645b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c645b-109">EXAMPLES</span></span>

### <span data-ttu-id="c645b-110">Przykład 1. Uzyskiwanie konta ANF</span><span class="sxs-lookup"><span data-stu-id="c645b-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="c645b-111">To polecenie pobiera konto o nazwie MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="c645b-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="c645b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c645b-112">PARAMETERS</span></span>

### <span data-ttu-id="c645b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c645b-113">-DefaultProfile</span></span>
<span data-ttu-id="c645b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c645b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c645b-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c645b-115">-Name</span></span>
<span data-ttu-id="c645b-116">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="c645b-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c645b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c645b-117">-ResourceGroupName</span></span>
<span data-ttu-id="c645b-118">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="c645b-118">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c645b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c645b-119">-ResourceId</span></span>
<span data-ttu-id="c645b-120">Identyfikator zasobu konta ANF</span><span class="sxs-lookup"><span data-stu-id="c645b-120">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c645b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c645b-121">CommonParameters</span></span>
<span data-ttu-id="c645b-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c645b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c645b-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c645b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c645b-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c645b-124">INPUTS</span></span>

### <span data-ttu-id="c645b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c645b-125">System.String</span></span>

## <span data-ttu-id="c645b-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c645b-126">OUTPUTS</span></span>

### <span data-ttu-id="c645b-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c645b-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="c645b-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c645b-128">NOTES</span></span>

## <span data-ttu-id="c645b-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c645b-129">RELATED LINKS</span></span>
