---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: d99487ed775efe5ea36c834f28ddb3c8c301182d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705765"
---
# <span data-ttu-id="568cc-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="568cc-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="568cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="568cc-102">SYNOPSIS</span></span>
<span data-ttu-id="568cc-103">Modyfikuje określonego zaufanego dostawcę tożsamości w określonej usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="568cc-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="568cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="568cc-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="568cc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="568cc-105">DESCRIPTION</span></span>
<span data-ttu-id="568cc-106">Polecenie cmdlet **Set-AzDataLakeStoreTrustedIdProvider** modyfikuje określonego zaufanego dostawcę tożsamości w określonej usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="568cc-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="568cc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="568cc-107">EXAMPLES</span></span>

### <span data-ttu-id="568cc-108">Przykład 1: aktualizowanie punktu końcowego zaufanego dostawcy tożsamości</span><span class="sxs-lookup"><span data-stu-id="568cc-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="568cc-109">Spowoduje to zaktualizowanie punktu końcowego dostawcy dla reguły zapory "mój operator" na koncie "ContosoADL" na " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="568cc-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="568cc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="568cc-110">PARAMETERS</span></span>

### <span data-ttu-id="568cc-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="568cc-111">-Account</span></span>
<span data-ttu-id="568cc-112">Konto usługi Data Lake Store umożliwiające dodanie dostawcy zaufanej tożsamości do</span><span class="sxs-lookup"><span data-stu-id="568cc-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="568cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="568cc-113">-DefaultProfile</span></span>
<span data-ttu-id="568cc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="568cc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="568cc-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="568cc-115">-Name</span></span>
<span data-ttu-id="568cc-116">Nazwa zaufanego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="568cc-116">The name of the trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="568cc-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="568cc-117">-ProviderEndpoint</span></span>
<span data-ttu-id="568cc-118">Prawidłowy punkt końcowy zaufanego dostawcy w formacie: https://sts.windows.net/\<provider tożsamość\></span><span class="sxs-lookup"><span data-stu-id="568cc-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="568cc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="568cc-119">-ResourceGroupName</span></span>
<span data-ttu-id="568cc-120">Określa nazwę grupy zasobów zawierającej konto, dla którego ma zostać zaktualizowany zaufany dostawca tożsamości.</span><span class="sxs-lookup"><span data-stu-id="568cc-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="568cc-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="568cc-121">-Confirm</span></span>
<span data-ttu-id="568cc-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="568cc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="568cc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="568cc-123">-WhatIf</span></span>
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

### <span data-ttu-id="568cc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="568cc-124">CommonParameters</span></span>
<span data-ttu-id="568cc-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="568cc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="568cc-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="568cc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="568cc-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="568cc-127">INPUTS</span></span>

### <span data-ttu-id="568cc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="568cc-128">System.String</span></span>

## <span data-ttu-id="568cc-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="568cc-129">OUTPUTS</span></span>

### <span data-ttu-id="568cc-130">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="568cc-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="568cc-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="568cc-131">NOTES</span></span>

## <span data-ttu-id="568cc-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="568cc-132">RELATED LINKS</span></span>
