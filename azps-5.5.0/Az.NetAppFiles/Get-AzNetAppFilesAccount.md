---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 677382133dffc7e64c86d02e984f35b8572a4598
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187307"
---
# <span data-ttu-id="907d2-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="907d2-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="907d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="907d2-102">SYNOPSIS</span></span>
<span data-ttu-id="907d2-103">Pobiera szczegółowe informacje o koncie usługi Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="907d2-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="907d2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="907d2-104">SYNTAX</span></span>

### <span data-ttu-id="907d2-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="907d2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="907d2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="907d2-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="907d2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="907d2-107">DESCRIPTION</span></span>
<span data-ttu-id="907d2-108">Polecenie **cmdlet Get-AzNetAppFilesAccount** pobiera szczegółowe informacje o koncie ANF.</span><span class="sxs-lookup"><span data-stu-id="907d2-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="907d2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="907d2-109">EXAMPLES</span></span>

### <span data-ttu-id="907d2-110">Przykład 1. Uzyskiwanie konta ANF</span><span class="sxs-lookup"><span data-stu-id="907d2-110">Example 1: Get an ANF account</span></span>
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

<span data-ttu-id="907d2-111">To polecenie pobiera konto o nazwie MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="907d2-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="907d2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="907d2-112">PARAMETERS</span></span>

### <span data-ttu-id="907d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907d2-113">-DefaultProfile</span></span>
<span data-ttu-id="907d2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="907d2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="907d2-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="907d2-115">-Name</span></span>
<span data-ttu-id="907d2-116">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="907d2-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="907d2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="907d2-117">-ResourceGroupName</span></span>
<span data-ttu-id="907d2-118">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="907d2-118">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="907d2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="907d2-119">-ResourceId</span></span>
<span data-ttu-id="907d2-120">Identyfikator zasobu konta ANF</span><span class="sxs-lookup"><span data-stu-id="907d2-120">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="907d2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907d2-121">CommonParameters</span></span>
<span data-ttu-id="907d2-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="907d2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907d2-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="907d2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907d2-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="907d2-124">INPUTS</span></span>

### <span data-ttu-id="907d2-125">System.String</span><span class="sxs-lookup"><span data-stu-id="907d2-125">System.String</span></span>

## <span data-ttu-id="907d2-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="907d2-126">OUTPUTS</span></span>

### <span data-ttu-id="907d2-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="907d2-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="907d2-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="907d2-128">NOTES</span></span>

## <span data-ttu-id="907d2-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="907d2-129">RELATED LINKS</span></span>
