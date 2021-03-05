---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: fc8e3d49f5c5a6430a6436b0d46e8fd10984db98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968625"
---
# <span data-ttu-id="56cbe-101">Get-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="56cbe-101">Get-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="56cbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56cbe-102">SYNOPSIS</span></span>
<span data-ttu-id="56cbe-103">Pobiera szczegółowe informacje o zasadach tworzenia kopii zapasowej plików ANF (Azure NetApp Files).</span><span class="sxs-lookup"><span data-stu-id="56cbe-103">Gets details of an Azure NetApp Files (ANF) Backup Policy.</span></span>

## <span data-ttu-id="56cbe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="56cbe-104">SYNTAX</span></span>

### <span data-ttu-id="56cbe-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="56cbe-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56cbe-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56cbe-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56cbe-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56cbe-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56cbe-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="56cbe-108">DESCRIPTION</span></span>
<span data-ttu-id="56cbe-109">Polecenie **cmdlet Get-AzNetAppFilesBackupPolicy** pobiera szczegółowe informacje o zasadach tworzenia kopii zapasowych ANF.</span><span class="sxs-lookup"><span data-stu-id="56cbe-109">The **Get-AzNetAppFilesBackupPolicy** cmdlet gets details of an ANF backup policy.</span></span>

## <span data-ttu-id="56cbe-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="56cbe-110">EXAMPLES</span></span>

### <span data-ttu-id="56cbe-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="56cbe-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="56cbe-112">To polecenie pobiera zasady kopii zapasowej o nazwie "MyBackupPolicy" dla konta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="56cbe-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="56cbe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56cbe-113">PARAMETERS</span></span>

### <span data-ttu-id="56cbe-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="56cbe-114">-AccountName</span></span>
<span data-ttu-id="56cbe-115">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="56cbe-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="56cbe-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="56cbe-116">-AccountObject</span></span>
<span data-ttu-id="56cbe-117">Obiekt Account zawierający zwracane zasady kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="56cbe-117">The Account object containing the Backup Policy to return</span></span>

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

### <span data-ttu-id="56cbe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56cbe-118">-DefaultProfile</span></span>
<span data-ttu-id="56cbe-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="56cbe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56cbe-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="56cbe-120">-Name</span></span>
<span data-ttu-id="56cbe-121">Nazwa zasad kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="56cbe-121">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56cbe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56cbe-122">-ResourceGroupName</span></span>
<span data-ttu-id="56cbe-123">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="56cbe-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="56cbe-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56cbe-124">-ResourceId</span></span>
<span data-ttu-id="56cbe-125">Identyfikator zasobu zasad kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="56cbe-125">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="56cbe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56cbe-126">CommonParameters</span></span>
<span data-ttu-id="56cbe-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56cbe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56cbe-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56cbe-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56cbe-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56cbe-129">INPUTS</span></span>

### <span data-ttu-id="56cbe-130">System.String</span><span class="sxs-lookup"><span data-stu-id="56cbe-130">System.String</span></span>

### <span data-ttu-id="56cbe-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="56cbe-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="56cbe-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56cbe-132">OUTPUTS</span></span>

### <span data-ttu-id="56cbe-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="56cbe-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="56cbe-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="56cbe-134">NOTES</span></span>

## <span data-ttu-id="56cbe-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56cbe-135">RELATED LINKS</span></span>
