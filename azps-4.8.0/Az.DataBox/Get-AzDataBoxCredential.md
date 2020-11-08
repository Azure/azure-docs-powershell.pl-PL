---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 308f7aa185350635815622ed684e47ebea349f9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064201"
---
# <span data-ttu-id="b13a3-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="b13a3-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="b13a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b13a3-102">SYNOPSIS</span></span>
<span data-ttu-id="b13a3-103">Pobiera poświadczenia DATAbox określonego zadania</span><span class="sxs-lookup"><span data-stu-id="b13a3-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="b13a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b13a3-104">SYNTAX</span></span>

### <span data-ttu-id="b13a3-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b13a3-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b13a3-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b13a3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b13a3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b13a3-107">DESCRIPTION</span></span>
<span data-ttu-id="b13a3-108">Polecenie cmdlet **Get-AzDataBoxCredential** Pobiera poświadczenia DATAbox określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="b13a3-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="b13a3-109">Wewnętrzne Właściwości zwróconego obiektu poświadczenia będą inne dla różnych typów jednostek SKU.</span><span class="sxs-lookup"><span data-stu-id="b13a3-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="b13a3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b13a3-110">EXAMPLES</span></span>

### <span data-ttu-id="b13a3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b13a3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="b13a3-112">To retuns JobSecrets określonego zadania</span><span class="sxs-lookup"><span data-stu-id="b13a3-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="b13a3-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b13a3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="b13a3-114">To retuns JobSecrets określonego zadania</span><span class="sxs-lookup"><span data-stu-id="b13a3-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="b13a3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b13a3-115">PARAMETERS</span></span>

### <span data-ttu-id="b13a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b13a3-116">-DefaultProfile</span></span>
<span data-ttu-id="b13a3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b13a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b13a3-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b13a3-118">-Name</span></span>
<span data-ttu-id="b13a3-119">Nazwa zadania DATAbox</span><span class="sxs-lookup"><span data-stu-id="b13a3-119">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13a3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b13a3-120">-ResourceGroupName</span></span>
<span data-ttu-id="b13a3-121">Nazwa grupy zasobów zadania DATAbox</span><span class="sxs-lookup"><span data-stu-id="b13a3-121">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13a3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b13a3-122">-ResourceId</span></span>
<span data-ttu-id="b13a3-123">Identyfikator zasobu zadania DATAbox</span><span class="sxs-lookup"><span data-stu-id="b13a3-123">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b13a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13a3-124">CommonParameters</span></span>
<span data-ttu-id="b13a3-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b13a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13a3-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b13a3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13a3-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b13a3-127">INPUTS</span></span>

### <span data-ttu-id="b13a3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b13a3-128">System.String</span></span>

## <span data-ttu-id="b13a3-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b13a3-129">OUTPUTS</span></span>

### <span data-ttu-id="b13a3-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Management. DataBox. MODELES. UnencryptedCredentials, Microsoft. Azure. Management. DataBox, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b13a3-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b13a3-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b13a3-131">NOTES</span></span>

## <span data-ttu-id="b13a3-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b13a3-132">RELATED LINKS</span></span>
