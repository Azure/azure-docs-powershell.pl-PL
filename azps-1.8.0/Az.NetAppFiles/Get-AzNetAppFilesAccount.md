---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: dbe206a744cc0a80d166d93b09ff0ab000cb3bc6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709751"
---
# <span data-ttu-id="8e616-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8e616-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="8e616-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e616-102">SYNOPSIS</span></span>
<span data-ttu-id="8e616-103">Pobiera szczegóły konta usługi Azure NetApp plików (ANF).</span><span class="sxs-lookup"><span data-stu-id="8e616-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="8e616-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e616-104">SYNTAX</span></span>

### <span data-ttu-id="8e616-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8e616-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e616-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e616-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e616-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8e616-107">DESCRIPTION</span></span>
<span data-ttu-id="8e616-108">Polecenie cmdlet **Get-AzNetAppFilesAccount** pobiera szczegóły konta ANF.</span><span class="sxs-lookup"><span data-stu-id="8e616-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="8e616-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e616-109">EXAMPLES</span></span>

### <span data-ttu-id="8e616-110">Przykład 1: Uzyskiwanie konta ANF</span><span class="sxs-lookup"><span data-stu-id="8e616-110">Example 1: Get an ANF account</span></span>
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

<span data-ttu-id="8e616-111">To polecenie uzyskuje konto o nazwie MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="8e616-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="8e616-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e616-112">PARAMETERS</span></span>

### <span data-ttu-id="8e616-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e616-113">-DefaultProfile</span></span>
<span data-ttu-id="8e616-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e616-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e616-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8e616-115">-Name</span></span>
<span data-ttu-id="8e616-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="8e616-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="8e616-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e616-117">-ResourceGroupName</span></span>
<span data-ttu-id="8e616-118">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="8e616-118">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8e616-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e616-119">-ResourceId</span></span>
<span data-ttu-id="8e616-120">Identyfikator zasobu konta ANF</span><span class="sxs-lookup"><span data-stu-id="8e616-120">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="8e616-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e616-121">CommonParameters</span></span>
<span data-ttu-id="8e616-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e616-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8e616-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e616-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e616-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e616-124">INPUTS</span></span>

### <span data-ttu-id="8e616-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8e616-125">System.String</span></span>

## <span data-ttu-id="8e616-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e616-126">OUTPUTS</span></span>

### <span data-ttu-id="8e616-127">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8e616-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="8e616-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e616-128">NOTES</span></span>

## <span data-ttu-id="8e616-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e616-129">RELATED LINKS</span></span>
