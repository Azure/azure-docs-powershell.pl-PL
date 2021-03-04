---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: f5f811b28b349c6dbc9972c9a464a56a002b99f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998698"
---
# <span data-ttu-id="fe0d7-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="fe0d7-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="fe0d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe0d7-102">SYNOPSIS</span></span>
<span data-ttu-id="fe0d7-103">Pobiera poświadczenia skrzynki danych dla określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="fe0d7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe0d7-104">SYNTAX</span></span>

### <span data-ttu-id="fe0d7-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe0d7-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe0d7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe0d7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe0d7-107">DESCRIPTION</span></span>
<span data-ttu-id="fe0d7-108">Polecenie **cmdlet Get-AzDataBoxCredential** pobiera poświadczenia pola danych określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="fe0d7-109">Właściwości wewnętrzne obiektu zwracanych poświadczeń będą się różnić w przypadku różnych typów elementów SKU.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="fe0d7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe0d7-110">EXAMPLES</span></span>

### <span data-ttu-id="fe0d7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fe0d7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="fe0d7-112">To retuns the JobSecrets of the specified job</span><span class="sxs-lookup"><span data-stu-id="fe0d7-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="fe0d7-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fe0d7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="fe0d7-114">To retuns the JobSecrets of the specified job</span><span class="sxs-lookup"><span data-stu-id="fe0d7-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="fe0d7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe0d7-115">PARAMETERS</span></span>

### <span data-ttu-id="fe0d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0d7-116">-DefaultProfile</span></span>
<span data-ttu-id="fe0d7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe0d7-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fe0d7-118">-Name</span></span>
<span data-ttu-id="fe0d7-119">Databox Job Name</span><span class="sxs-lookup"><span data-stu-id="fe0d7-119">Databox Job Name</span></span>

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

### <span data-ttu-id="fe0d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe0d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="fe0d7-121">Databox Job Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="fe0d7-121">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="fe0d7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe0d7-122">-ResourceId</span></span>
<span data-ttu-id="fe0d7-123">Identyfikator zasobu zadania w skrzynce danych</span><span class="sxs-lookup"><span data-stu-id="fe0d7-123">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="fe0d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0d7-124">CommonParameters</span></span>
<span data-ttu-id="fe0d7-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe0d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe0d7-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe0d7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0d7-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe0d7-127">INPUTS</span></span>

### <span data-ttu-id="fe0d7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="fe0d7-128">System.String</span></span>

## <span data-ttu-id="fe0d7-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe0d7-129">OUTPUTS</span></span>

### <span data-ttu-id="fe0d7-130">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="fe0d7-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="fe0d7-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe0d7-131">NOTES</span></span>

## <span data-ttu-id="fe0d7-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe0d7-132">RELATED LINKS</span></span>
