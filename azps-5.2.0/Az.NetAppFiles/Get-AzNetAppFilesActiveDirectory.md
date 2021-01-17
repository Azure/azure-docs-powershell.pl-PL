---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 6c082d2e61f81c4e0b8cf9bebefd623584fac3e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360110"
---
# <span data-ttu-id="9ff0d-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="9ff0d-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="9ff0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ff0d-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff0d-103">Pobiera szczegóły konfiguracji usługi Active Directory w usłudze Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="9ff0d-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="9ff0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ff0d-104">SYNTAX</span></span>

### <span data-ttu-id="9ff0d-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9ff0d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ff0d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ff0d-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ff0d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9ff0d-107">DESCRIPTION</span></span>
<span data-ttu-id="9ff0d-108">Polecenie cmdlet **Get-AzNetAppFilesActiveDirectory** pobiera szczegóły konfiguracji usługi Active Directory konta ANF.</span><span class="sxs-lookup"><span data-stu-id="9ff0d-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="9ff0d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ff0d-109">EXAMPLES</span></span>

### <span data-ttu-id="9ff0d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9ff0d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="9ff0d-111">To polecenie uzyskuje konfigurację usługi AD o nazwie MyADConfigName dla konta usługi Azure NetApp Files (ANF) o nazwie MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="9ff0d-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="9ff0d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ff0d-112">PARAMETERS</span></span>

### <span data-ttu-id="9ff0d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9ff0d-113">-AccountName</span></span>
<span data-ttu-id="9ff0d-114">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="9ff0d-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="9ff0d-115">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="9ff0d-115">-AccountObject</span></span>
<span data-ttu-id="9ff0d-116">Konto nowego obiektu usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="9ff0d-116">The Account for the new Active Directory object</span></span>

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

### <span data-ttu-id="9ff0d-117">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="9ff0d-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="9ff0d-118">ActiveDirectoryId usługi ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="9ff0d-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

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

### <span data-ttu-id="9ff0d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff0d-119">-DefaultProfile</span></span>
<span data-ttu-id="9ff0d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ff0d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ff0d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ff0d-121">-ResourceGroupName</span></span>
<span data-ttu-id="9ff0d-122">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="9ff0d-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="9ff0d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff0d-123">CommonParameters</span></span>
<span data-ttu-id="9ff0d-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ff0d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff0d-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ff0d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff0d-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ff0d-126">INPUTS</span></span>

### <span data-ttu-id="9ff0d-127">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="9ff0d-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="9ff0d-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ff0d-128">OUTPUTS</span></span>

### <span data-ttu-id="9ff0d-129">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="9ff0d-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="9ff0d-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ff0d-130">NOTES</span></span>

## <span data-ttu-id="9ff0d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ff0d-131">RELATED LINKS</span></span>
