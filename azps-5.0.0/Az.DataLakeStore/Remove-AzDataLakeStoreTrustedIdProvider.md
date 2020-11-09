---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 3e16db29f6560778dff5c86ac222d06fd41a5807
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305521"
---
# <span data-ttu-id="0bffe-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="0bffe-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="0bffe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0bffe-102">SYNOPSIS</span></span>
<span data-ttu-id="0bffe-103">Usuwa określonego zaufanego dostawcę tożsamości w określonej usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0bffe-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="0bffe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0bffe-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0bffe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0bffe-105">DESCRIPTION</span></span>
<span data-ttu-id="0bffe-106">Polecenie cmdlet **Remove-AzDataLakeStoreTrustedIdProvider** usuwa określonego zaufanego dostawcę tożsamości w określonej usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0bffe-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="0bffe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0bffe-107">EXAMPLES</span></span>

### <span data-ttu-id="0bffe-108">Przykład 1: usunięcie zaufanego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="0bffe-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="0bffe-109">Usuwa dostawcę "The dostarczająca" z konta "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="0bffe-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="0bffe-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0bffe-110">PARAMETERS</span></span>

### <span data-ttu-id="0bffe-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="0bffe-111">-Account</span></span>
<span data-ttu-id="0bffe-112">Konto usługi Data Lake Store do usunięcia zaufanego dostawcy tożsamości</span><span class="sxs-lookup"><span data-stu-id="0bffe-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="0bffe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bffe-113">-DefaultProfile</span></span>
<span data-ttu-id="0bffe-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0bffe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bffe-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0bffe-115">-Name</span></span>
<span data-ttu-id="0bffe-116">Nazwa zaufanego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="0bffe-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="0bffe-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bffe-117">-PassThru</span></span>
<span data-ttu-id="0bffe-118">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="0bffe-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="0bffe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bffe-119">-ResourceGroupName</span></span>
<span data-ttu-id="0bffe-120">Określa nazwę grupy zasobów zawierającej konto, z którego należy usunąć zaufanego dostawcę tożsamości.</span><span class="sxs-lookup"><span data-stu-id="0bffe-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="0bffe-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0bffe-121">-Confirm</span></span>
<span data-ttu-id="0bffe-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bffe-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bffe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bffe-123">-WhatIf</span></span>
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

### <span data-ttu-id="0bffe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bffe-124">CommonParameters</span></span>
<span data-ttu-id="0bffe-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bffe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bffe-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bffe-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bffe-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bffe-127">INPUTS</span></span>

### <span data-ttu-id="0bffe-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0bffe-128">System.String</span></span>

### <span data-ttu-id="0bffe-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0bffe-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0bffe-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0bffe-130">OUTPUTS</span></span>

### <span data-ttu-id="0bffe-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0bffe-131">System.Boolean</span></span>

## <span data-ttu-id="0bffe-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0bffe-132">NOTES</span></span>

## <span data-ttu-id="0bffe-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0bffe-133">RELATED LINKS</span></span>
