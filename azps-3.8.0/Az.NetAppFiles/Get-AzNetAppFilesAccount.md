---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: eb30f07e0443712e7287ae850f463070f5aca3f3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894229"
---
# <span data-ttu-id="ea94a-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ea94a-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="ea94a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea94a-102">SYNOPSIS</span></span>
<span data-ttu-id="ea94a-103">Pobiera szczegóły konta usługi Azure NetApp plików (ANF).</span><span class="sxs-lookup"><span data-stu-id="ea94a-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="ea94a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea94a-104">SYNTAX</span></span>

### <span data-ttu-id="ea94a-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ea94a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea94a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea94a-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea94a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ea94a-107">DESCRIPTION</span></span>
<span data-ttu-id="ea94a-108">Polecenie cmdlet **Get-AzNetAppFilesAccount** pobiera szczegóły konta ANF.</span><span class="sxs-lookup"><span data-stu-id="ea94a-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="ea94a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea94a-109">EXAMPLES</span></span>

### <span data-ttu-id="ea94a-110">Przykład 1: Uzyskiwanie konta ANF</span><span class="sxs-lookup"><span data-stu-id="ea94a-110">Example 1: Get an ANF account</span></span>
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

<span data-ttu-id="ea94a-111">To polecenie uzyskuje konto o nazwie MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="ea94a-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="ea94a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea94a-112">PARAMETERS</span></span>

### <span data-ttu-id="ea94a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea94a-113">-DefaultProfile</span></span>
<span data-ttu-id="ea94a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea94a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea94a-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea94a-115">-Name</span></span>
<span data-ttu-id="ea94a-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="ea94a-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea94a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea94a-117">-ResourceGroupName</span></span>
<span data-ttu-id="ea94a-118">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="ea94a-118">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea94a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea94a-119">-ResourceId</span></span>
<span data-ttu-id="ea94a-120">Identyfikator zasobu konta ANF</span><span class="sxs-lookup"><span data-stu-id="ea94a-120">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea94a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea94a-121">CommonParameters</span></span>
<span data-ttu-id="ea94a-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea94a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ea94a-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea94a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea94a-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea94a-124">INPUTS</span></span>

### <span data-ttu-id="ea94a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ea94a-125">System.String</span></span>

## <span data-ttu-id="ea94a-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea94a-126">OUTPUTS</span></span>

### <span data-ttu-id="ea94a-127">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ea94a-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="ea94a-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea94a-128">NOTES</span></span>

## <span data-ttu-id="ea94a-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea94a-129">RELATED LINKS</span></span>
