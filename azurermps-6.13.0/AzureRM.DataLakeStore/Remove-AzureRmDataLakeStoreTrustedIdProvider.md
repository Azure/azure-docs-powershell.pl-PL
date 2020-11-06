---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: f281192e22cd8acdf85e389d82ef7146590be158
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524441"
---
# <span data-ttu-id="ab314-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="ab314-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="ab314-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab314-102">SYNOPSIS</span></span>
<span data-ttu-id="ab314-103">Usuwa określonego zaufanego dostawcę tożsamości w określonej usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab314-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab314-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab314-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab314-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ab314-105">DESCRIPTION</span></span>
<span data-ttu-id="ab314-106">Polecenie cmdlet **Remove-AzureRmDataLakeStoreTrustedIdProvider** usuwa określonego zaufanego dostawcę tożsamości w określonej usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab314-106">The **Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="ab314-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab314-107">EXAMPLES</span></span>

### <span data-ttu-id="ab314-108">Przykład 1: usunięcie zaufanego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ab314-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="ab314-109">Usuwa dostawcę "The dostarczająca" z konta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="ab314-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="ab314-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab314-110">PARAMETERS</span></span>

### <span data-ttu-id="ab314-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="ab314-111">-Account</span></span>
<span data-ttu-id="ab314-112">Konto usługi Data Lake Store do usunięcia zaufanego dostawcy tożsamości</span><span class="sxs-lookup"><span data-stu-id="ab314-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab314-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab314-113">-DefaultProfile</span></span>
<span data-ttu-id="ab314-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ab314-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab314-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ab314-115">-Name</span></span>
<span data-ttu-id="ab314-116">Nazwa zaufanego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ab314-116">The name of the trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab314-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab314-117">-PassThru</span></span>
<span data-ttu-id="ab314-118">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="ab314-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab314-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab314-119">-ResourceGroupName</span></span>
<span data-ttu-id="ab314-120">Określa nazwę grupy zasobów zawierającej konto, z którego należy usunąć zaufanego dostawcę tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ab314-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab314-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab314-121">-Confirm</span></span>
<span data-ttu-id="ab314-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab314-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab314-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab314-123">-WhatIf</span></span>
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

### <span data-ttu-id="ab314-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab314-124">CommonParameters</span></span>
<span data-ttu-id="ab314-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab314-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab314-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab314-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab314-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab314-127">INPUTS</span></span>

### <span data-ttu-id="ab314-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ab314-128">System.String</span></span>

### <span data-ttu-id="ab314-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ab314-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ab314-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab314-130">OUTPUTS</span></span>

### <span data-ttu-id="ab314-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab314-131">System.Boolean</span></span>

## <span data-ttu-id="ab314-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab314-132">NOTES</span></span>

## <span data-ttu-id="ab314-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab314-133">RELATED LINKS</span></span>
