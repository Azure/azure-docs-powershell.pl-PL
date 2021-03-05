---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 7198e34e7e888c2e89fce6cb5293bfc46bf57b1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968641"
---
# <span data-ttu-id="fb9cb-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="fb9cb-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="fb9cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb9cb-102">SYNOPSIS</span></span>
<span data-ttu-id="fb9cb-103">Pobiera szczegółowe informacje o konfiguracji usługi Active Directory w usłudze Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="fb9cb-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="fb9cb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fb9cb-104">SYNTAX</span></span>

### <span data-ttu-id="fb9cb-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="fb9cb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb9cb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb9cb-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb9cb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fb9cb-107">DESCRIPTION</span></span>
<span data-ttu-id="fb9cb-108">Polecenie **cmdlet Get-AzNetAppFilesActiveDirectory** pobiera szczegółowe informacje o konfiguracji konta ANF w usłudze Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="fb9cb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fb9cb-109">EXAMPLES</span></span>

### <span data-ttu-id="fb9cb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fb9cb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="fb9cb-111">To polecenie pobiera konfigurację usługi AD o nazwie MyADConfigName dla konta usługi Azure NetApp Files (ANF) o nazwie MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="fb9cb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb9cb-112">PARAMETERS</span></span>

### <span data-ttu-id="fb9cb-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fb9cb-113">-AccountName</span></span>
<span data-ttu-id="fb9cb-114">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="fb9cb-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="fb9cb-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="fb9cb-115">-AccountObject</span></span>
<span data-ttu-id="fb9cb-116">Konto nowego obiektu usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="fb9cb-116">The Account for the new Active Directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9cb-117">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="fb9cb-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="fb9cb-118">ActiveDirectoryId usługi Active Directory ANF</span><span class="sxs-lookup"><span data-stu-id="fb9cb-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActiveDirectoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9cb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb9cb-119">-DefaultProfile</span></span>
<span data-ttu-id="fb9cb-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb9cb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb9cb-121">-ResourceGroupName</span></span>
<span data-ttu-id="fb9cb-122">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="fb9cb-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="fb9cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb9cb-123">CommonParameters</span></span>
<span data-ttu-id="fb9cb-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb9cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb9cb-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb9cb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb9cb-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb9cb-126">INPUTS</span></span>

### <span data-ttu-id="fb9cb-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="fb9cb-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="fb9cb-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb9cb-128">OUTPUTS</span></span>

### <span data-ttu-id="fb9cb-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="fb9cb-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="fb9cb-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fb9cb-130">NOTES</span></span>

## <span data-ttu-id="fb9cb-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb9cb-131">RELATED LINKS</span></span>
