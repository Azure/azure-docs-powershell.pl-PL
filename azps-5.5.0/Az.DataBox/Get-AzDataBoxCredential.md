---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 308f7aa185350635815622ed684e47ebea349f9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181138"
---
# <span data-ttu-id="65f05-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="65f05-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="65f05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65f05-102">SYNOPSIS</span></span>
<span data-ttu-id="65f05-103">Pobiera poświadczenia skrzynki danych dla określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="65f05-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="65f05-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="65f05-104">SYNTAX</span></span>

### <span data-ttu-id="65f05-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="65f05-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65f05-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65f05-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65f05-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="65f05-107">DESCRIPTION</span></span>
<span data-ttu-id="65f05-108">Polecenie **cmdlet Get-AzDataBoxCredential** pobiera poświadczenia pola danych określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="65f05-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="65f05-109">Właściwości wewnętrzne obiektu zwracanych poświadczeń będą się różnić w przypadku różnych typów elementów SKU.</span><span class="sxs-lookup"><span data-stu-id="65f05-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="65f05-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="65f05-110">EXAMPLES</span></span>

### <span data-ttu-id="65f05-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="65f05-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="65f05-112">To retuns the JobSecrets of the specified job</span><span class="sxs-lookup"><span data-stu-id="65f05-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="65f05-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="65f05-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="65f05-114">To retuns the JobSecrets of the specified job</span><span class="sxs-lookup"><span data-stu-id="65f05-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="65f05-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65f05-115">PARAMETERS</span></span>

### <span data-ttu-id="65f05-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65f05-116">-DefaultProfile</span></span>
<span data-ttu-id="65f05-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="65f05-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65f05-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="65f05-118">-Name</span></span>
<span data-ttu-id="65f05-119">Databox Job Name</span><span class="sxs-lookup"><span data-stu-id="65f05-119">Databox Job Name</span></span>

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

### <span data-ttu-id="65f05-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65f05-120">-ResourceGroupName</span></span>
<span data-ttu-id="65f05-121">Databox Job Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="65f05-121">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="65f05-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65f05-122">-ResourceId</span></span>
<span data-ttu-id="65f05-123">Identyfikator zasobu zadania w skrzynce danych</span><span class="sxs-lookup"><span data-stu-id="65f05-123">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="65f05-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f05-124">CommonParameters</span></span>
<span data-ttu-id="65f05-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65f05-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f05-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65f05-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f05-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65f05-127">INPUTS</span></span>

### <span data-ttu-id="65f05-128">System.String</span><span class="sxs-lookup"><span data-stu-id="65f05-128">System.String</span></span>

## <span data-ttu-id="65f05-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65f05-129">OUTPUTS</span></span>

### <span data-ttu-id="65f05-130">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="65f05-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="65f05-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="65f05-131">NOTES</span></span>

## <span data-ttu-id="65f05-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65f05-132">RELATED LINKS</span></span>
