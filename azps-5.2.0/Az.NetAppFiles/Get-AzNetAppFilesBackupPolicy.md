---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 754149172b3154975580a0802426f9a2f20c0f62
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360087"
---
# <span data-ttu-id="76e42-101">Get-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="76e42-101">Get-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="76e42-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76e42-102">SYNOPSIS</span></span>
<span data-ttu-id="76e42-103">Pobiera szczegóły zasad tworzenia kopii zapasowej plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="76e42-103">Gets details of an Azure NetApp Files (ANF) Backup Policy.</span></span>

## <span data-ttu-id="76e42-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76e42-104">SYNTAX</span></span>

### <span data-ttu-id="76e42-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="76e42-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76e42-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76e42-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76e42-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76e42-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76e42-108">Opis</span><span class="sxs-lookup"><span data-stu-id="76e42-108">DESCRIPTION</span></span>
<span data-ttu-id="76e42-109">Polecenie cmdlet **Get-AzNetAppFilesBackupPolicy** pobiera szczegółowe informacje o ANFych zasadach tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="76e42-109">The **Get-AzNetAppFilesBackupPolicy** cmdlet gets details of an ANF backup policy.</span></span>

## <span data-ttu-id="76e42-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76e42-110">EXAMPLES</span></span>

### <span data-ttu-id="76e42-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76e42-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="76e42-112">To polecenie pobiera zasady tworzenia kopii zapasowych o nazwie "MyBackupPolicy" dla konta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="76e42-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="76e42-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76e42-113">PARAMETERS</span></span>

### <span data-ttu-id="76e42-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="76e42-114">-AccountName</span></span>
<span data-ttu-id="76e42-115">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="76e42-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="76e42-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="76e42-116">-AccountObject</span></span>
<span data-ttu-id="76e42-117">Obiekt konta zawierający zasady tworzenia kopii zapasowych do zwrócenia</span><span class="sxs-lookup"><span data-stu-id="76e42-117">The Account object containing the Backup Policy to return</span></span>

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

### <span data-ttu-id="76e42-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76e42-118">-DefaultProfile</span></span>
<span data-ttu-id="76e42-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76e42-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76e42-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76e42-120">-Name</span></span>
<span data-ttu-id="76e42-121">Nazwa zasad tworzenia kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="76e42-121">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="76e42-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76e42-122">-ResourceGroupName</span></span>
<span data-ttu-id="76e42-123">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="76e42-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="76e42-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76e42-124">-ResourceId</span></span>
<span data-ttu-id="76e42-125">Identyfikator zasobu zasad tworzenia kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="76e42-125">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="76e42-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e42-126">CommonParameters</span></span>
<span data-ttu-id="76e42-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76e42-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76e42-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76e42-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e42-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76e42-129">INPUTS</span></span>

### <span data-ttu-id="76e42-130">System. String</span><span class="sxs-lookup"><span data-stu-id="76e42-130">System.String</span></span>

### <span data-ttu-id="76e42-131">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="76e42-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="76e42-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76e42-132">OUTPUTS</span></span>

### <span data-ttu-id="76e42-133">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="76e42-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="76e42-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76e42-134">NOTES</span></span>

## <span data-ttu-id="76e42-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76e42-135">RELATED LINKS</span></span>
