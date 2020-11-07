---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: d7290d44a1e6a08b79ccb5a0b5ff88ec482b4875
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888121"
---
# <span data-ttu-id="13526-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="13526-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="13526-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13526-102">SYNOPSIS</span></span>
<span data-ttu-id="13526-103">Usuwa zasady zarządzania konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="13526-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="13526-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13526-104">SYNTAX</span></span>

### <span data-ttu-id="13526-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="13526-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13526-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="13526-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13526-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="13526-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13526-108">Policyobject</span><span class="sxs-lookup"><span data-stu-id="13526-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13526-109">Opis</span><span class="sxs-lookup"><span data-stu-id="13526-109">DESCRIPTION</span></span>
<span data-ttu-id="13526-110">Polecenie cmdlet **Remove-AzStorageAccountManagementPolicy** usuwa zasady zarządzania konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="13526-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="13526-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13526-111">EXAMPLES</span></span>

### <span data-ttu-id="13526-112">Przykład 1: usuwanie zasad zarządzania konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="13526-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="13526-113">To polecenie usuwa zasady zarządzania konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="13526-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="13526-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13526-114">PARAMETERS</span></span>

### <span data-ttu-id="13526-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13526-115">-DefaultProfile</span></span>
<span data-ttu-id="13526-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13526-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13526-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="13526-117">-InputObject</span></span>
<span data-ttu-id="13526-118">Obiekt zarządzania do usunięcia</span><span class="sxs-lookup"><span data-stu-id="13526-118">Management Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: PolicyObject
Aliases: ManagementPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13526-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13526-119">-PassThru</span></span>
<span data-ttu-id="13526-120">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="13526-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="13526-121">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="13526-121">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13526-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13526-122">-ResourceGroupName</span></span>
<span data-ttu-id="13526-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="13526-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13526-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="13526-124">-StorageAccount</span></span>
<span data-ttu-id="13526-125">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="13526-125">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13526-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="13526-126">-StorageAccountName</span></span>
<span data-ttu-id="13526-127">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="13526-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13526-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="13526-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="13526-129">Identyfikator zasobu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="13526-129">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13526-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13526-130">-Confirm</span></span>
<span data-ttu-id="13526-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13526-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13526-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13526-132">-WhatIf</span></span>
<span data-ttu-id="13526-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13526-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13526-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13526-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13526-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13526-135">CommonParameters</span></span>
<span data-ttu-id="13526-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13526-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13526-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13526-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13526-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13526-138">INPUTS</span></span>

### <span data-ttu-id="13526-139">System. String</span><span class="sxs-lookup"><span data-stu-id="13526-139">System.String</span></span>

## <span data-ttu-id="13526-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13526-140">OUTPUTS</span></span>

### <span data-ttu-id="13526-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13526-141">System.Boolean</span></span>

## <span data-ttu-id="13526-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13526-142">NOTES</span></span>

## <span data-ttu-id="13526-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13526-143">RELATED LINKS</span></span>
