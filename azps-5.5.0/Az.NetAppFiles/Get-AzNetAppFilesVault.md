---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: 9779db097028710aa8aeddc7a5a1c5bdea85a30a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241146"
---
# <span data-ttu-id="1cd63-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="1cd63-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="1cd63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cd63-102">SYNOPSIS</span></span>
<span data-ttu-id="1cd63-103">Pobiera listę magazynów kopii zapasowych kont usługi Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="1cd63-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="1cd63-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1cd63-104">SYNTAX</span></span>

### <span data-ttu-id="1cd63-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1cd63-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cd63-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cd63-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1cd63-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cd63-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cd63-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1cd63-108">DESCRIPTION</span></span>
<span data-ttu-id="1cd63-109">Polecenie **cmdlet Get-AzNetAppFilesVault** pobiera listę magazynów kopii zapasowych kont ANF.</span><span class="sxs-lookup"><span data-stu-id="1cd63-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="1cd63-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1cd63-110">EXAMPLES</span></span>

### <span data-ttu-id="1cd63-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1cd63-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="1cd63-112">To polecenie otrzymuje listę magazynów kopii zapasowej dla konta Azure NetappFiles (ANF) "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="1cd63-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="1cd63-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cd63-113">PARAMETERS</span></span>

### <span data-ttu-id="1cd63-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1cd63-114">-AccountName</span></span>
<span data-ttu-id="1cd63-115">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="1cd63-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cd63-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="1cd63-116">-AccountObject</span></span>
<span data-ttu-id="1cd63-117">Konto nowego obiektu kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="1cd63-117">The account for the new backup object</span></span>

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

### <span data-ttu-id="1cd63-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cd63-118">-DefaultProfile</span></span>
<span data-ttu-id="1cd63-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1cd63-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cd63-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cd63-120">-ResourceGroupName</span></span>
<span data-ttu-id="1cd63-121">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="1cd63-121">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="1cd63-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cd63-122">-ResourceId</span></span>
<span data-ttu-id="1cd63-123">Identyfikator zasobu puli ANF</span><span class="sxs-lookup"><span data-stu-id="1cd63-123">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="1cd63-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cd63-124">CommonParameters</span></span>
<span data-ttu-id="1cd63-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cd63-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cd63-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1cd63-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cd63-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1cd63-127">INPUTS</span></span>

### <span data-ttu-id="1cd63-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1cd63-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="1cd63-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1cd63-129">System.String</span></span>

## <span data-ttu-id="1cd63-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1cd63-130">OUTPUTS</span></span>

### <span data-ttu-id="1cd63-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="1cd63-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="1cd63-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1cd63-132">NOTES</span></span>

## <span data-ttu-id="1cd63-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1cd63-133">RELATED LINKS</span></span>
