---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: 9779db097028710aa8aeddc7a5a1c5bdea85a30a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360026"
---
# <span data-ttu-id="faffb-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="faffb-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="faffb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="faffb-102">SYNOPSIS</span></span>
<span data-ttu-id="faffb-103">Pobiera listę magazynów kopii zapasowych kont usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="faffb-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="faffb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="faffb-104">SYNTAX</span></span>

### <span data-ttu-id="faffb-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="faffb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="faffb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="faffb-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="faffb-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="faffb-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faffb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="faffb-108">DESCRIPTION</span></span>
<span data-ttu-id="faffb-109">Polecenie cmdlet **Get-AzNetAppFilesVault** pobiera listę magazynów kopii zapasowych kont ANF.</span><span class="sxs-lookup"><span data-stu-id="faffb-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="faffb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="faffb-110">EXAMPLES</span></span>

### <span data-ttu-id="faffb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="faffb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="faffb-112">To polecenie uzyskuje listę magazynów kopii zapasowych dla konta usługi Azure NetappFiles (ANF) "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="faffb-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="faffb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="faffb-113">PARAMETERS</span></span>

### <span data-ttu-id="faffb-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="faffb-114">-AccountName</span></span>
<span data-ttu-id="faffb-115">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="faffb-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="faffb-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="faffb-116">-AccountObject</span></span>
<span data-ttu-id="faffb-117">Konto nowego obiektu kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="faffb-117">The account for the new backup object</span></span>

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

### <span data-ttu-id="faffb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faffb-118">-DefaultProfile</span></span>
<span data-ttu-id="faffb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="faffb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faffb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faffb-120">-ResourceGroupName</span></span>
<span data-ttu-id="faffb-121">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="faffb-121">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="faffb-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="faffb-122">-ResourceId</span></span>
<span data-ttu-id="faffb-123">Identyfikator zasobu puli ANF</span><span class="sxs-lookup"><span data-stu-id="faffb-123">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="faffb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faffb-124">CommonParameters</span></span>
<span data-ttu-id="faffb-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faffb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faffb-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="faffb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faffb-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="faffb-127">INPUTS</span></span>

### <span data-ttu-id="faffb-128">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="faffb-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="faffb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="faffb-129">System.String</span></span>

## <span data-ttu-id="faffb-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="faffb-130">OUTPUTS</span></span>

### <span data-ttu-id="faffb-131">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="faffb-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="faffb-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="faffb-132">NOTES</span></span>

## <span data-ttu-id="faffb-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="faffb-133">RELATED LINKS</span></span>
